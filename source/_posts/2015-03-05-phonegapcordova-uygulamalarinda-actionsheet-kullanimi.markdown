---
layout: post
title: PhoneGap/Cordova uygulamalarında ActionSheet kullanımı
date: 2015-03-05 21:22:40.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- cordova
- javascript
- Jquery
tags:
- action sheet
- alertdialog
- android
- cordova actionsheet
- ios
- windows phone
---
<p>Action Sheet  native olarak kullanıcıya seçenek listesinden birşey seçtirmek için kullanabileceginiz bir plugindir.  Birçok uygulamada görebilirsiniz. ( Yazının sonundaki görsele bakarsanız daha anlaşılır olabilir.) Plugin iOS, Android ve Windows Phone platformlarını desteklemektedir.</p>
<p>Şimdi  basit bir uygulama oluştururak  nasıl kullanıldığını görelim.</p>
<pre class="theme:github lang:default decode:true">//
cordova create actionsheet com.example.actionsheet ActionSheet
//
cd  actionsheet

//
cordova platform add android

//</pre>
<p>ActionSheet pluginini ekliyoruz ve hazırlıyoruz.</p>
<pre class="lang:default decode:true">cordova plugin add https://github.com/EddyVerbruggen/cordova-plugin-actionsheet
//
 cordova prepare</pre>
<p>Demo olarak bu kodu inceleyebilirsiniz. oldukça basit Javascript kodu oldugu için açıklamaya gerek yok diye düşünüyorum.</p>
<pre class="theme:github lang:default decode:true">&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta charset="utf-8" /&gt;
    &lt;meta name="format-detection" content="telephone=no" /&gt;
    &lt;!-- WARNING: for iOS 7, remove the width=device-width and height=device-height attributes. See https://issues.apache.org/jira/browse/CB-4323 --&gt;
    &lt;meta name="viewport" content="user-scalable=no, initial-scale=1, maximum-scale=1, minimum-scale=1, width=device-width, height=device-height" /&gt;
    &lt;link rel="stylesheet" type="text/css" href="css/index.css" /&gt;
    &lt;meta name="msapplication-tap-highlight" content="no" /&gt;
    &lt;title&gt;Hello ActionSheet&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;div class="app"&gt;
    &lt;h1&gt;ActionSheet demo&lt;/h1&gt;
    &lt;div id="deviceready" class="blink"&gt;
        &lt;p class="event listening"&gt;Connecting to Device&lt;/p&gt;
        &lt;p class="event received"&gt;Device is Ready&lt;/p&gt;
        &lt;button onclick="testShareSheet()"&gt;Test Share&lt;/button&gt;&lt;br/&gt;&lt;br/&gt;
        &lt;button onclick="testDeleteSheet()"&gt;Test Delete&lt;/button&gt;&lt;br/&gt;&lt;br/&gt;
        &lt;button onclick="testLogoutSheet()"&gt;Test Logout&lt;/button&gt;
    &lt;/div&gt;
&lt;/div&gt;
&lt;script type="text/javascript" src="cordova.js"&gt;&lt;/script&gt;
&lt;script type="text/javascript" src="js/index.js"&gt;&lt;/script&gt;
&lt;script type="text/javascript"&gt;

    app.initialize();

    var callback = function(buttonIndex) {
        setTimeout(function() {
            alert('button index clicked: ' + buttonIndex);
        });
    };

    function testShareSheet() {
        var options = {
            'androidTheme' : window.plugins.actionsheet.ANDROID_THEMES.THEME_HOLO_LIGHT,
            'title': 'What do you want with this image?',
            'buttonLabels': ['Share via Facebook', 'Share via Twitter'],
            'addCancelButtonWithLabel': 'Cancel',
            'androidEnableCancelButton' : true,
            'winphoneEnableCancelButton' : true,
            'addDestructiveButtonWithLabel' : 'Delete it'
        };
        window.plugins.actionsheet.show(options, callback);
    }

    function testDeleteSheet() {
        var options = {
            'addCancelButtonWithLabel': 'Cancel',
            'addDestructiveButtonWithLabel' : 'Delete note'
        };
        window.plugins.actionsheet.show(options, callback);
    }

    function testLogoutSheet() {
        var options = {
            'buttonLabels': ['Log out'],
            'androidEnableCancelButton' : true,
            'winphoneEnableCancelButton' : true,
            'addCancelButtonWithLabel': 'Cancel'
        };
        window.plugins.actionsheet.show(options, callback);
    }

&lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
</pre>
<p><a href="https://github.com/EddyVerbruggen/cordova-plugin-actionsheet">ActionSheet Github sayfasını ziyaret edip daha fazla bilgi alabilirsiniz.</a></p>
<p><a href="http://www.nazirdogan.com/wp-content/uploads/2015/03/snapshot41.png"><img class="alignnone size-full wp-image-760" src="{{ site.baseurl }}/assets/snapshot41.png" alt="snapshot41" width="532" height="819" /></a></p>
