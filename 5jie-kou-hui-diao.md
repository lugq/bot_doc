# 回调接口



回调接口示例：

```
TtCloudManager.setCallBack(new TtCloudListener() {
            @Override
            public void onBack(ImageView iv_back) {
                
            }

            @Override
            public boolean onShare(Article article, User user, ResultCallBack callBack) {
                return false;
            }

            @Override
            public boolean onLiked(Article article, User user) {
                return false;
            }

            @Override
            public boolean onComment(Article article, User user) {
                return false;
            }
        });
```



