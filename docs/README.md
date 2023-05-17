# Jetpack Compose Cookbook📚

## README😝

这里记录的是作者在大二课程上Android开发技术基础课程时使用jetpack compose所记录的一些常用代码段和一些开发经验share出来，希望对大伙有用。

$$
Code_\text{平时记录}>>Code_\text{结课设计}
$$

> 这里安利一波金旭亮老师去年的课程视频（在今年的课程中引入了很多compose的内容）：[2022北理Android开发技术基础](https://space.bilibili.com/612518983/channel/collectiondetail?sid=320093)
>
> `Composable`意为可重组的，在最后的进行结课设计的开发中自己也用到了很多平时写的简单组件，在这里希望把这些组件设计share出来，方便之后的重用，也同时方便其它开发者的使用😭😭😭。
>
> 目前网上传统的android项目基本都是基于view的开发，由于采用了compose开发，自己在踩了不少坑，最后在进行开发的时候进行参考的例子（包括本文档的代码段）大多来自于下面这些地方：

| 评价                                                         | 参考网站                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| 首推官方文档👉                                                | https://developer.android.com/                               |
| 还有官方的code lab也是一绝，比如👉                            | [Compose 中的 ViewModel 和状态 (android.com)](https://developer.android.com/codelabs/basic-android-kotlin-compose-viewmodel-and-state?hl=zh-cn#5) |
| 有很多最新的开发技术、或者将旧技术迁移到compose上的方法的网站👉 | https://proandroiddev.com/                                   |
| youtube上讲的很清晰的示例以及代码的示例，比如👉               | https://www.youtube.com/watch?v=tD0wi5sH0aQ                  |

> 几乎很少用chatgpt，因为它给出来的很多关于compose的代码几乎都是错的，或者说没有这个功能。

### PS：本项目的想法来源🔗

创建这个文件夹是受老师的影响，看到老师把相应的一些常用的代码放在自己写的一个个人资料管理的软件里面，但是感觉自己使用Typora就可以完全实现这个功能了，后期如果做的很好用的话，我们一样可以创建自己的snippet，这种按tab就可以自动补全（结合IDE的功能）也很快，虽然在自己开发中也使用了Copilot这样的插件，但很多时候对于一个大的工程文件或者项目文件、又或者最新的Compose技术，Copilot就不能保证了（在`Copilot`有时停机跟不上代码生成的速度话、从代码的可运行程度来说还是自己的代码库质量更高一点）。

> Anyway, hope it helps you~🍰 
