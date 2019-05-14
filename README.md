@[TOC](实验五)
# Intent
## 自定义WebView验证隐式Intent的使用
![在这里插入图片描述](https://img-blog.csdnimg.cn/20190514110140297.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMjQxNDEy,size_16,color_FFFFFF,t_70)
public class MainActivity extends AppCompatActivity {
    private static final String TAG ="fff" ;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button button1 = (Button)findViewById(R.id.b1);
        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                EditText editText = (EditText)findViewById(R.id.e1);
                String text = editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW);
                intent.setData(Uri.parse(text));
//                intent.putExtra("url",text);
                startActivity(intent);
            }
        });
    }

}

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190514112437853.jpg?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQyMjQxNDEy,size_16,color_FFFFFF,t_70)
