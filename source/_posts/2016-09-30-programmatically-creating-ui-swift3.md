---
layout: post
title: Programmatically creating UI elements using Swift 3
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
  - swift 3 ui
  - uiview
  - uislider
  - uiswitch
  - Button
  - Segmented Controls
  - Sliders
  - Steppers
  - Switches
  - UISegmentedControl Programmatically
  - UISwitches Programmatically
  - UIButton Programmatically
  - UISlider Programmatically
  - iOS 10
  - Swift 3 Programmatically UI Elements

---

if you are new in iOS development and using Interface Builder for creating UI elements. Maybe you want to learn how can do with code. In this post I will talk about this and give a snippet.



### UIView

```swift

let child = UIView(frame: CGRect(x: 100, y: 100,width:100, height: 100))
child.backgroundColor = UIColor.red
self.view.addSubview(child)

```

<img src="/assets/Simulator Screen Shot 30 Sep 2016 13.19.40.png" width="308">

### UISlider

```swift
 let slider = UISlider (frame: CGRect(x: 10, y: 300,width:300, height: 100))
     slider.minimumValue = 0
     slider.maximumValue = 100
     slider.tintColor = UIColor.red
     slider.isContinuous = true
     slider.value = 30
     slider.addTarget(self, action:#selector(sliderValueDidChange), for: .valueChanged)
     self.view.addSubview(slider)
```

```swift
func sliderValueDidChange(sender:UISlider!)
   {
      print("value : \(sender.value)")
   }

```

<img src="/assets/Simulator Screen Shot 30 Sep 2016 13.56.51.png" width="308">


### UIButton

```swift
let button  = UIButton (frame : CGRect (x:100, y:100 ,width:100 , height:40))
    button.backgroundColor = UIColor.red
    button.setTitle("My Button", for:.normal)
    button.setTitleColor(UIColor.yellow, for: .normal)
   self.view.addSubview(button)
```



```swift
 button.addTarget(self, action: #selector(buttonClicked), for: .touchUpInside)
```




<img src="/assets/Simulator Screen Shot 30 Sep 2016 14.56.26.png" width="308">


### UISwitch


```swift

let switchDemo = UISwitch(frame: CGRect(x:100, y:100 ,width:40, height:40))
    switchDemo.isOn  = true
    switchDemo.addTarget(self, action: #selector(switchChanged), for: .valueChanged)
    self.view.addSubview(switchDemo)

```

```swift

func switchChanged(sender: UISwitch!){

      print("value: \(sender.isOn)")
  }

```
<img src="/assets/Simulator Screen Shot 30 Sep 2016 19.40.40.png" width="308">



### UISegmentedControl


```swift
let segmentedControl = UISegmentedControl(frame: CGRect(x:10, y:100 ,width:260, height:30))
    segmentedControl.insertSegment(withTitle:"index 0", at: 0, animated: false)
    segmentedControl.insertSegment(withTitle:"index 1", at: 1, animated: false)
    segmentedControl.insertSegment(withTitle:"index 2", at: 2, animated: false)
    segmentedControl.addTarget(self, action: #selector(getSegmentedControlValue), for: .valueChanged)
    segmentedControl.selectedSegmentIndex = 0
    self.view.addSubview(segmentedControl)

```

```swift
func getSegmentedControlValue(sender:UISegmentedControl!) {
       if  sender.selectedSegmentIndex == 0 {
           print("index 0")

       }
       else if sender.selectedSegmentIndex == 1 {

           print("index 1")

       }
       else {
           print("index 2")
       }

   }

```

<img src="/assets/Simulator Screen Shot 30 Sep 2016 19.43.35.png" width="308">
