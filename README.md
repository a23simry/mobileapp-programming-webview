
# Rapport

Bytte namn på appen och tilllät internet. Skapade en webview i rätt layout fil, gav den en ID och skrev kod så att den skapas i OnCreate() med rätt ID. Skapade sedan en webviewclient och satte den på webviewen och ändrade dens javascript inställningar. lade till två html länkar i string, och skrev kod så att de laddas när man klickar på dropdown menyn. 


```
<resources>
    <string name="app_name">Web wieving</string>
    <string name="action_external_web">External Web Page</string>
    <string name="action_internal_web">Internal Web Page</string>
    <string name="my_link"><![CDATA[https://simonrydberg.xyz/]]></string>
    <string name="my_link2"><![CDATA[https://student.his.se/]]></string>
</resources>

private WebView myWebView;
private WebViewClient webViewClient;

public void showExternalWebPage(){
    // TODO: Add your code for showing external web page here
    myWebView.loadUrl(getString(R.string.my_link2));
}

public void showInternalWebPage(){
    // TODO: Add your code for showing internal web page here
    myWebView.loadUrl(getString(R.string.my_link));

}

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    Toolbar toolbar = findViewById(R.id.toolbar);
    setSupportActionBar(toolbar);

    myWebView = findViewById(R.id.my_webview);
    myWebView.setWebViewClient(webViewClient);
    myWebView.getSettings().setJavaScriptEnabled(true);

}


if (id == R.id.action_external_web) {
    Log.d("==>","Will display external web page");
    showExternalWebPage();
    return true;
}

if (id == R.id.action_internal_web) {
    Log.d("==>","Will display internal web page");
    showInternalWebPage();
    return true;
}


<WebView
    android:id="@+id/my_webview"
    android:layout_width="411dp"
    android:layout_height="674dp"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent" />

```


![](bild1.png)
![](bild2.png)

