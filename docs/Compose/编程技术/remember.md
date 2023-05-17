# remember

## 导入库（如果不希望按几次alt+enter的话）

```kotlin
import androidx.compose.runtime.remember
import androidx.compose.runtime.mutableStateOf
import androidx.compose.runtime.getValue
import androidx.compose.runtime.setValue
```

## 简单用法

```kotlin
var shouldShowOnboarding by remember { mutableStateOf(true) }
```

像上面这条语句执行过后我们就可以在当前app状态下记住它的值：

```kotlin
@Composable
fun MyApp(){
    // TODO: This state should be hoisted
    var shouldShowOnboarding by remember { mutableStateOf(true) }

    if (shouldShowOnboarding){
        OnboardingScreen(onContinueClicked = { shouldShowOnboarding = false })
    } else {
        Greetings()
    }
}
```

如果希望在全局状态改变时（旋转屏幕、暗夜模式）也记住可以改成：

```kotlin
var shouldShowOnboarding by rememberSaveable { mutableStateOf(true) }
```

再也不想手动点五六次下面才导入下面这个（直接复制）

```kotlin
import androidx.compose.runtime.*
```



