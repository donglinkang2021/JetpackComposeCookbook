# Image



> 说是Image，但这里更多的想介绍一下的是如何从网络拉去图片资源并加载

## AsyncImage

AndroidManifest中添加

```kotlin
<uses-permission android:name="android.permission.INTERNET" />
...
android:usesCleartextTraffic="true"
```

build.gradle中添加

```kotlin
implementation("io.coil-kt:coil-compose:2.3.0")

//添加协程相关的依赖
def coroutines_version = "1.6.4"
implementation "org.jetbrains.kotlinx:kotlinx-coroutines-core:$coroutines_version"
implementation "org.jetbrains.kotlinx:kotlinx-coroutines-android:$coroutines_version"
```

显示网络图片

```kotlin
AsyncImage(
    model = "https://tse3-mm.cn.bing.net/th/id/OIP-C.lhA01NkPpyrvK2O-h_rChgHaKf?pid=ImgDet&rs=1",
    contentDescription = "从网站上下载的图片"
    contentScale = ContentScale.Crop,
    modifier = Modifier
        .fillMaxWidth()
)
```

