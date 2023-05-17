# LazyColumn

用`LazyColumn`可以解决加载元素很多时候的问题，比如下面，在一个页面中如果我们只想显示看到的那部分控件的显示就可以不全部加载出来，把下面代码：

```
names.forEach { name ->
	Greeting(name)
}
```

改成：

```kotlin
LazyColumn(){
    items(names) { name ->
    	Greeting(name)
    }
}
```

使用它的时候通常都会和`items`结合起来，但这里的`items`会使用默认的而报错(说类型不匹配，而Android studio不会自动给你提示import)，这时候我们记得在最开头：

```kotlin
import androidx.compose.foundation.lazy.items
```



**源代码**

```kotlin
@Composable
fun Greetings(names: List<String> = List(1000) { "Android #$it" }) {
    // A surface container using the 'background' color from the theme
    Surface(
        color = MaterialTheme.colors.background
    ) {
        Column (
            modifier = Modifier.padding(vertical = 8.dp)
                ){
            LazyColumn(){
                item { Text(text = "Header") }
                items(names) { name ->
                    Greeting(name)
                }
            }
        }
    }
}
```

