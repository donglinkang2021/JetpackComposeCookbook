# ViewModel

## 例子一

### Activity

```kotlin
// Path: MainActivity.kt

@Composable
fun MyApp() {
    //实例化ViewModel
    val vm: MyViewModel = viewModel()
    //将LiveData转换为Compose可观察的状态
    val info by vm.currentTime.observeAsState()

    Column(
        ...
    ) {
        Button(onClick = {
            vm.whatTimeIs()
        }) {
            ...
        }
        ...
        Text(
            text = info ?: "未知时间",
            ...
        )
    }
}
```

### ViewModel

```kotlin
// Path: MyViewModel.kt

class MyViewModel : ViewModel() {
    private val _currentTime = MutableLiveData<String>()
    val currentTime: LiveData<String>
        get() = _currentTime

    fun whatTimeIs() {
        _currentTime.value = "当前时间：${LocalTime.now()}"
    }
}
```



## 例子二

参考官方code lab：

[Compose 中的 ViewModel 和状态 (android.com)](https://developer.android.com/codelabs/basic-android-kotlin-compose-viewmodel-and-state?hl=zh-cn#5)
