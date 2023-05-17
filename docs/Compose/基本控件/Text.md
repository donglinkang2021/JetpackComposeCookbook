# Text

```kotlin
Text(
    text = stringResource(id = R.string.app_name),
    style = MaterialTheme.typography.bodyLarge
)
```

可上下滑动text

```kotlin
Text(
    text = text.value,
    modifier = Modifier
        .fillMaxSize()
        .verticalScroll(rememberScrollState())
        .padding(10.dp)
)
```

调整字体大小要注意是sp为单位，如果是dp会报错

```
Text(
            text = text, // 显示的文本
            fontSize = 30.sp, // 字体大小为 14dp
            color = DrawColors.PredictionText, // 文本颜色为主题中的 PredictionText 颜色
            modifier = modifier
//                .padding(horizontal = 16.dp, vertical = 8.dp) // 左右间距为 16dp，上下间距为 8dp
                .padding(2.dp)
                .clickable { onClick.invoke(text) }, // 添加点击事件，点击时调用 onClick 方法并传入文本内容
        )
```

