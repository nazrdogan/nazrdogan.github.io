---
layout: post
title: Getting Started with Titanium Alloy MVC Framework
date: 2015-12-07 17:36:00.000000000 +02:00
type: post
published: true
comments: true
status: publish
categories:
- titanium mobile
tags:
- alloy
- alloy mvc tutorial
- appcelerator
- getting started with alloy
- titanium alloy mvc
- titanium mobile
---
<p class="p1"><strong><span class="s1">What is Alloy ?</span></strong></p>
<p class="p1"><span class="s1">Alloy is a MVC framework by Appcelerator for developer to build cross platform application . Titanium have two way for developing mobile apps. One of them named Titanium classic and second one is Titanium alloy. You are not required to alloy framework .you can still continue classic one . But you will not have alloy benefits. </span></p>
<p class="p1"><strong><span class="s1">Let's look alloy mvc</span></strong></p>
<p class="p1"><strong>Model</strong></p>
<p class="p1"><span class="s1">The model store data local or remote.it can be SQLite , file or web service data.no matter what is data type. Model layer is doing managing or manipulating data.if you heard CRUD  you know what I'm talking about.</span></p>
<p class="p1">
<p class="p1"><a href="http://www.nazirdogan.com/wp-content/uploads/2015/12/Screen-Shot-2015-12-07-at-18.07.57.png"><img class="alignnone wp-image-939 size-medium" src="{{ site.baseurl }}/assets/Screen-Shot-2015-12-07-at-18.07.57-244x300.png" alt="Screen Shot 2015-12-07 at 18.07.57" width="244" height="300" /></a></p>
<p class="p1">you can create model in project folder like this and as well as the other components.</p>
<pre class="theme:sublime-text lang:default decode:true">exports.definition = {
	config: {

		adapter: {
			type: "sql",
			collection_name: "firstmodel"
		}
	},
	extendModel: function(Model) {
		_.extend(Model.prototype, {
			// extended functions and properties go here
		});

		return Model;
	},
	extendCollection: function(Collection) {
		_.extend(Collection.prototype, {
			// extended functions and properties go here

			// For Backbone v1.1.2, uncomment the following to override the
			// fetch method to account for a breaking change in Backbone.
			/*
			fetch: function(options) {
				options = options ? _.clone(options) : {};
				options.reset = true;
				return Backbone.Collection.prototype.fetch.call(this, options);
			}
			*/
		});

		return Collection;
	}
};</pre>
<p>&nbsp;</p>
<p class="p1"><span class="s1">The view is very simple and easy to understand .its the presentation layer of the application. Users will interact with this layer.</span>If you know xml you know alloy view . Because it's only xml.</p>
<pre class="theme:sublime-text lang:default decode:true ">&lt;Alloy&gt;
	&lt;Window class="container"&gt;
		&lt;Label id="label" onClick="doClick"&gt;Hello, World&lt;/Label&gt;
	&lt;/Window&gt;
&lt;/Alloy&gt;</pre>
<p>and you can change your view style with  TSS files. its inside styles folder. TSS  similar to CSS but it uses JSON-like syntax.</p>
<pre class="theme:sublime-text lang:default decode:true">".container": {
	backgroundColor:"white"
}

"Label": {
	width: Ti.UI.SIZE,
	height: Ti.UI.SIZE,
	color: "#000"
}

"#label": {
	font: {
		fontSize: 12
	}
}
</pre>
<p><strong><span class="s1">Controller</span></strong></p>
<p class="p1"><span class="s1">Controller is business logic your application.its glue between model and views.</span></p>
<pre class="theme:sublime-text lang:default decode:true ">function doClick(e) {
    alert($.label.text);
}

$.index.open();
</pre>
<p>you can see doClick function in your view. When user interact label on device screen. doClick will work.</p>
<p>if you create Controller in your alloy project with Appcelerator Studio. Studio will create view(.xml) and style(.tss) files. and will be named same your controller.</p>
<p>For Example:  you create home.js  controller and created file home.xml and home.tss .But if you do this manually. you must add other files manually.</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
