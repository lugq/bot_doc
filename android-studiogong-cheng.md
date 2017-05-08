## Android Studio工程

1.请在工程文件根目录下创建一个名为 libs 的子目录，并将360广告 SDK 的 aar 包拷贝到 libs 目录下;

2.`build.gradle`中配置如下：

```
...
dependencies {
    ...
    compile(name: 'bot-video-05-031505', ext: 'aar')

    compile 'com.android.support:support-v4:25.1.0'
    compile 'com.android.support:appcompat-v7:25.1.0'
    compile 'com.google.code.gson:gson:2.8.0'
    compile 'com.nostra13.universalimageloader:universal-image-loader:1.9.5'

    ...
}

repositories {
    flatDir {
        dirs 'libs'
    }
}
```





