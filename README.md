# TabContainerView
Android TabContainerView 实现底部导航栏效果

 ![image](https://github.com/chenpengfei88/TabContainerView/blob/master/app/src/main/res/drawable/xiaoguo.gif)
 
 # 使用
 
 public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        initView();
    }

    private void initView() {
        TabContainerView tabContainerView = (TabContainerView) findViewById(R.id.tab_containerview_main);

        tabContainerView.setAdapter(new MainTabContainerAdapter(getSupportFragmentManager(),
                new Fragment[] {new MainFragment(), new WorkFragment(), new AppFragment(), new MineFragment()}));

        tabContainerView.setOnTabSelectedListener(new OnTabSelectedListener() {
            @Override
            public void onTabSelected(Tab tab) {
            }
        });
    }
}


