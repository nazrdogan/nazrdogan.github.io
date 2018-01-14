---
layout: post
title: Integrating  jshint in ionic framework
date: 2015-08-02 17:02:52.000000000 +03:00
type: post
published: true
comments: true
status: publish
categories:
- Angular.js
- cordova
- javascript
tags:
- cordova ionic
- ionic
- ionic jshint
- jshint
---
<p>if you are developing ionic apps.  you can see build system in your projects which is  Gulp . it's not ionic specific but it's used in ionic projects and many other project ,its so similar to Grunt.</p>
<p>in this post ,I write about how can save time  with linting javascript files  in your ionic project.</p>
<p>&nbsp;</p>
<p>Let's create an ionic project</p>
<pre class="theme:solarized-dark lang:default decode:true">//
ionic start jshint-ionic

//in your project folder

 npm install


</pre>
<p>After creating an ionic project for using JSHint ,we must load gulp-jshint and  js<span class="s1">hint-stylish  from npm.</span></p>
<pre class="theme:solarized-dark lang:js decode:true">//


npm install gulp-jshint jshint-stylish --save-dev


//</pre>
<p>We installed gulp-jshint and jshint-stylish. jshint-stylish is not necessary but make output looks good.</p>
<p>After that we must edit gulpfile.js include this line of code.</p>
<pre class="theme:solarized-dark lang:js decode:true">//

var  jshint = require('gulp-jshint');

//</pre>
<p>then add gulp  task</p>
<pre class="theme:solarized-dark lang:default decode:true ">//


gulp.task('lint', function() {
  return gulp.src('./www/js/*.js')
    .pipe(jshint())
    .pipe(jshint.reporter('jshint-stylish'));
});


//</pre>
<p>&nbsp;</p>
<p>Now you can run  <strong>gulp lint</strong>  command  see syntax and logical error.</p>
<p>if you want to watch jshint  then add this line in "watch" task</p>
<pre class="theme:solarized-dark lang:default decode:true">//


gulp.task('watch', function() {
  gulp.watch(paths.sass, ['sass']);

    gulp.watch('./www/js/app/*.js', ['lint']);
});

//</pre>
<p>you dont write <strong>gulp lint</strong> command. if you serve your project jshint works automatically.</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
