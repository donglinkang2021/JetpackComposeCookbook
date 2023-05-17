# by

```kotlin
var shouldShowOnboarding by remember { mutableStateOf(true) }
```

用`by`的最直接好处是`remember { mutableStateOf(true) }`返回的是一个 state，如果直接用`=`那么我们在后续调用`shouldShowOnboarding`的时候得在后面加个`.value`

```kotlin
var shouldShowOnboarding = remember { mutableStateOf(true) }
shouldShowOnboarding.value ...
```



> 个人感觉上by后面老是加个什么State，从而实现一个变量的附加状态



加了`mutableStateOf`需要注意的添加的依赖库：

```
import androidx.compose.runtime.mutableStateOf
import androidx.compose.runtime.getValue
import androidx.compose.runtime.setValue

var userGuess by mutableStateOf("")
   private set
```

