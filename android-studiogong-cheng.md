## Android Studio工程

1.请在工程文件根目录下创建一个名为 libs 的子目录，并将图文的 SDK 中 aar 包拷贝到 libs 目录下;

1. `build.gradle`中配置如下：

```
...
dependencies {
    ...
    compile(name: 'bot-video-xx', ext: 'aar')

    // 需要添加的依赖    
    compile 'com.android.support:support-v4:25.1.0'
    compile 'com.android.support:appcompat-v7:25.1.0'

    compile 'com.google.code.gson:gson:2.8.0'
    compile 'com.github.bumptech.glide:glide:4.0.0-RC1'
    annotationProcessor 'com.github.bumptech.glide:compiler:4.0.0-RC1'

    ...
}

repositories {
    flatDir {
        dirs 'libs'
    }
}
```

3.`Sync Project` 完成。

