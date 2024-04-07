
# Rapport

Bytte namn på appen och tilllät internet. Skapade en webview i rätt layout fil, gav den en ID och skrev kod så att den skapas i OnCreate() med rätt ID. Skapade sedan en webviewclient och satte den på webviewen och ändrade dens javascript inställningar. lade till två html länkar i string, och skrev kod så att de laddas när man klickar på dropdown menyn. 

**Skriv din rapport här!**

_Du kan ta bort all text som finns sedan tidigare_.

## Följande grundsyn gäller dugga-svar:

- Ett kortfattat svar är att föredra. Svar som är längre än en sida text (skärmdumpar och programkod exkluderat) är onödigt långt.
- Svaret skall ha minst en snutt programkod.
- Svaret skall inkludera en kort övergripande förklarande text som redogör för vad respektive snutt programkod gör eller som svarar på annan teorifråga.
- Svaret skall ha minst en skärmdump. Skärmdumpar skall illustrera exekvering av relevant programkod. Eventuell text i skärmdumpar måste vara läsbar.
- I de fall detta efterfrågas, dela upp delar av ditt svar i för- och nackdelar. Dina för- respektive nackdelar skall vara i form av punktlistor med kortare stycken (3-4 meningar).

Programkod ska se ut som exemplet nedan. Koden måste vara korrekt indenterad då den blir lättare att läsa vilket gör det lättare att hitta syntaktiska fel.

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

Bilder läggs i samma mapp som markdown-filen.

![](bild1.png)
![](bild2.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
