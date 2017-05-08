# 接入图文

在`Activity`中打开图文的页面如下：

```
public class MainActivity extends FragmentActivity {

    private NewsIndexFragment mNewsIndexFragment;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        mNewsIndexFragment = new NewsIndexFragment();
    }
    
    // 打开NewsIndexFragment即可
    public void openNews(View view) {
        if (!mNewsIndexFragment.isAdded()) {
            FragmentManager fragmentManager = getSupportFragmentManager();
            FragmentTransaction fragmentTransaction = fragmentManager.beginTransaction();
            fragmentTransaction.add(R.id.container, mNewsIndexFragment);
            fragmentTransaction.commit();
        }
    }

}
```



