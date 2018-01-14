---
layout: post
title: Swift 3 Dersleri-Temeller
date: 2016-9-30
type: post
published: true
comments: true
status: publish
categories:
  - iOS
  - swift 3
tags:
  - swift
  - swift 3
  - swift 3 değişken
  - swift 3 sabitler

---

<img src="/assets/swift_logo.png" width="100%">


## Merhaba Dünya uygulaması

```swift
print("Merhaba Dünya")
```					

### Değişken Tanımlama

```swift
var myName = "Nazır"
var myNumber = 13
```		

### Sabit Tanımlama 

```swift
let myName = "Nazır"
```		

### Veri Tipleri

```swift

	// Character veri tipi
	var character :Character = "N"
	
	// String Veri Tipi
	var myName: String = "Nazır"
	
	// Int Veri Tipi
	var myNumber: Int = 13
	
	// Float ve Double veri tipi
	
	var number:Float = 4.2
	
	var number2:Double = 1.1
	
	// sabitlerde bu şekilde yazılabilir
	let myName:String = "Nazır"
```	

### For döngüsü oluşturma

```swift
	for var x in 0..<10 {
		print(x)
	}
```		

### Switch case yapısı

```swift	
	let name = "Nazır"
	// 'break' yazmak gerekmez.
	switch name {
	 case "Nazır" : print("Merhaba Nazır")
	 case "Damla" : print("Merhaba Damla")
	 default : print("Merhaba")
	}
```	

### While Döngüsü

```swift
var x = 0
	
// 0'dan 9 a kadar sayar
while x<10 {
  print(x)
	x++
}
```					

### If Else yapısı

```swift	
let swiftIsCool = true
	
if swiftIsCool {
	print("Tabi Canım")
}
else {
	print("Hayır")
	}
```	
