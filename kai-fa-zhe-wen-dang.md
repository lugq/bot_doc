添加scheme调用

```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="xx.xx.xx">

    <application
        ...
        android:theme="@style/AppTheme">
        
        <!--  设置申请的 AppId 和 AppKey -->
        <meta-data android:name="TTC_APPID" android:value="申请的AppId" />
        <meta-data android:name="TTC_APPKEY" android:value="申请的AppKey" />
              
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>

        <!-- 深度链接功能需要添加以下配置 -->
        <intent-filter>
            <action android:name="android.intent.action.VIEW" />

            <category android:name="android.intent.category.DEFAULT" />
            <category android:name="android.intent.category.BROWSABLE" />

            <data android:scheme="bot-news" />

        </intent-filter>
        ...
    </application>

</manifest>
```



