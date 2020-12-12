# <p align="center"> Binding </p>

<p align="center">
一行代码实现 DataBinding 和 ViewBinding，欢迎 start<br/>
<p align="center">
<a href="https://github.com/hi-dhl"><img src="https://img.shields.io/badge/GitHub-HiDhl-4BC51D.svg?style=flat"></a> <a href="https://opensource.org/licenses/Apache-2.0"><img src="https://img.shields.io/badge/license-Apache2.0-blue.svg?style=flat"></a> <img src="https://img.shields.io/badge/language-kotlin-orange.svg"/> <img src="https://img.shields.io/badge/platform-android-lightgrey.svg"/>
</p>
</p>

<p align="center">
<image src="http://img.hi-dhl.com/carbon.png" width = 600px/>
</p>


* 兼容了 DataBinding 和 ViewBinding 两种方式
* 避免模板代码，只需要一行代码即可实现 DataBinding 或者 ViewBinding 
* 避免内存泄露

## Download

**Gradle**

将下列代码添加进模块 build.gradle 文件内，并且开启 DataBinding 或者 ViewBinding

```

android {
    buildFeatures {
        dataBinding = true
        viewBinding = true
    }
}

dependencies {
    implementation 'com.hi-dhl:binding:1.0.0'
}
```


## Usage

在 `Activity` 、`AppCompatActivity` 、`FragmentActivity` 使用方式如下所示。

```
class MainActivity : AppCompatActivity() {

    // DataBinding
    val binding: ActivityMainBinding by databind(R.layout.activity_main)
    // ViewBinding
    // val binding: ActivityMainBinding by viewbind()

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        binding.apply {
            textView.setText("Binding")
        }
    }
}
```

在 `Fragment` 使用方式如下所示。

```
class MainFragment : Fragment(R.layout.fragment_main) {
    // DataBinding
  	val binding: FragmentMainBinding by databind()
    // ViewBinding
  	// val binding: FragmentMainBinding by viewbind()
  
    override fun onViewCreated(view: View, savedInstanceState: Bundle?) {
        super.onViewCreated(view, savedInstanceState)
        binding.apply { textView.setText("Binding") }
    }
}
```

### 联系我

* 个人微信：hi-dhl
* 公众号：ByteCode，包含 Jetpack ，Kotlin ，Android 10 系列源码，译文，LeetCode / 剑指 Offer / 多线程 / 国内外大厂算法题 等等一系列文章

<img src='http://cdn.51git.cn/2020-10-20-151047.png' width = 350px/>

---

最后推荐我一直在更新维护的项目和网站：

* 计划建立一个最全、最新的 AndroidX Jetpack 相关组件的实战项目 以及 相关组件原理分析文章，正在逐渐增加 Jetpack 新成员，仓库持续更新，欢迎前去查看：[AndroidX-Jetpack-Practice](https://github.com/hi-dhl/AndroidX-Jetpack-Practice)

* LeetCode / 剑指 offer / 国内外大厂面试题 / 多线程 题解，语言 Java 和 kotlin，包含多种解法、解题思路、时间复杂度、空间复杂度分析<br/>

    <image src="http://cdn.51git.cn/2020-10-04-16017884626310.jpg" width = "500px"/>
  
    * 剑指 offer 及国内外大厂面试题解：[在线阅读](https://offer.hi-dhl.com)
    * LeetCode 系列题解：[在线阅读](https://leetcode.hi-dhl.com)

* 最新 Android 10 源码分析系列文章，了解系统源码，不仅有助于分析问题，在面试过程中，对我们也是非常有帮助的，仓库持续更新，欢迎前去查看 [Android10-Source-Analysis](https://github.com/hi-dhl/Android10-Source-Analysis)

* 整理和翻译一系列精选国外的技术文章，每篇文章都会有**译者思考**部分，对原文的更加深入的解读，仓库持续更新，欢迎前去查看 [Technical-Article-Translation](https://github.com/hi-dhl/Technical-Article-Translation)

* 「为互联网人而设计，国内国外名站导航」涵括新闻、体育、生活、娱乐、设计、产品、运营、前端开发、Android 开发等等网址，欢迎前去查看 [为互联网人而设计导航网站](https://site.51git.cn)
