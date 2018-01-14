---
layout: post
title: Passing Data Parent to Child Controller - Titanium Alloy
date: 2015-12-24T19:29:07.000Z
type: post
published: true
comments: true
status: publish
categories:
  - titanium mobile
tags:
  - Alloy Passing Data
  - Titanium Alloy Controller
  - titanium mobile
---

In this post , I will give small snippet about passing data parent to child controller.

```
//index.js

function goDetail(e){

$.tab.open(Alloy.createController('detail',{data:e.row.title}).getView());
}
$.index.open();



```

```
//index.xml
<Alloy>
    <TabGroup>
         <Tab id="tab">
       <Window onClick="goDetail" id="win" backgroundColor="white" navBarHidden="true" tabBarHidden="true">
        <TableView id="table">
                <TableViewRow title="Apple"/>
                <TableViewRow title="Bananas"/><br>
<TableViewRow title="Carrots"/>
                <TableViewRow title="Potatoes"/>
                 <TableViewRow title="Cod"/>
                <TableViewRow title="Haddock"/><br>
</TableView>
    </Window>
    </Tab>
    </TabGroup>
</Alloy>
```



```
// detail.js
var args = arguments[0] || {};
 Ti.API.info(args.data);
  $.title.text=args.data;

//detail.xml
<Alloy>
    <Window class="container" backgroundColor="white">
     <Label top=30 id="title"><Label>
    </Window>
</Alloy>
```



<iframe width="420" height="315" src="https://www.youtube.com/embed/qQUshuYvP1w" frameborder="0" allowfullscreen="allowfullscreen">
</iframe>
