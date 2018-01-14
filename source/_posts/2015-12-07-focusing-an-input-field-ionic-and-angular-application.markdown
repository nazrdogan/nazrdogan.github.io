---
layout: post
title: Focusing an input Field Ionic and Angular Application.
date: 2015-12-07 21:30:49.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- Angular.js
- cordova
- javascript
- phonegap
tags:
- angular
- angularjs
- focusing input
- html5
- ionic
---
<p>if you developing Angular/Ionic application. Maybe you need to focusing input field. with this small code snippet is very easy.</p>
<pre class="theme:sublime-text lang:default decode:true">factory('focus', function($timeout, $window) {
        return function(id) {
            $timeout(function() {
                var element = $window.document.getElementById(id);
                if(element)
                    element.focus();
            });
        };
    });</pre>
<p>&nbsp;</p>
<p>Full example on <a href="http://codepen.io/nazrdogan_/pen/VeYpVJ">Codepen</a></p>
<p>&nbsp;</p>
