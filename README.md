<!-- <img src="logo.jpg" /> -->

## Quick Start

### Get it [![gitTio](http://gitt.io/badge.svg)](http://gitt.io/component/ti.material)

*Proudly developed at [Caffeina](http://caffeina.com)*

-

#### Module to port [Google Material Design](http://www.google.com/design/spec/material-design/introduction.html) to Titanium, specifically iOS!

Thanks to [FPT Software](http://www.fpt-software.com/) for developing a great [library](https://github.com/fpt-software/Material-Controls-For-iOS) that made this possible.

>The module is being developed for both iOS and Android to bring more features to Android as well, although for the moment the iOS version is usable while the Android version is in an early stage.

UI elements supported by the native library vs. ti.material

UI | Original | ti.material (iOS) | ti.material (Android)
--- | ---| --- | ----
MDButton | :x: | :x: | :o:
MDTableViewCell | :x: | :o: | :o:
MDProgress | :x: | :x: | :o:
MDSlider | :x: | :o: | :o:
MDSwitch | :x: | :x: | :o:
MDTabBar | :x: | :o: | :o:
MDTabBarViewController | :x: | :o: | :o:
MDTextField | :x: | :x: | :o:
MDSnackbar | :x: | :o: | :o:
MDToast | :x: | :x: | :o:
MDDatePicker | :x: | :x: | :o:
MDTimePicker | :x: | :x: | :o:

<image src="http://i.imgur.com/HZ5465U.png" width="40%"/>
<image src="http://i.imgur.com/YhSj7k0.png"  width="40%"/>
<image src="http://i.imgur.com/GVs8pR0.png" width="40%"/>
<image src="http://i.imgur.com/paB5ieB.png" width="40%"/>


## Install the module

Unzip the latest release in your module directory and add to tiapp modules, then add the module to **tiapp.xml**

```xml
<module platform="ios">ti.material</module>
```

or through gitTio

```bash
$ gittio install ti.material
```

Initialize it as below

```javascript
var Material = require("ti.material");
```

## MDButton

Creating a button is very straightforward. 

```javascript
var button = Material.createButton({});
```

The button accepts the following list of properties:

### Properties

Property | Type | Default | Description
--- | --- | --- | ----
title | String | App Title | The title to show in the notification center.
color | String | n/a | The color of the button title
touchFeedbackColor | String | n/a | The color of the ripple effect of the button
backgroundColor | String | n/a | The color of the button background
style | int | 0 | The style of the button going from 0 to 3. The last two being FAB
font | font object | system font | The font of the button title
enabled | Bool | true | Determines whether the element is enabled or not
opacity | float | 1.0 | Opacity of the element
rotated | Bool | false | Sets the rotation status of the FAB (style 3) button
imageNormal | String | null | The image instead of the title for a FAB button in the not rotated state
imageRotated | String | null | Same as above but for the rotated state of the button

### Events

Inherited from titanium:

- touchstart
- touchend
- touchmove
- touchcancel
- click
- dblclick

new:

- rotationstarted
- rotationcompleted

## MDSwitch

To create a switch use the following code. 

```javascript
var switch_ = Material.createSwitch({});
```

It accepts these properties:

### Properties

Property | Type | Default | Description
--- | --- | --- | ----
height | float | Ti.UI.FILL | This property doesn't change the size of the actual switch but it's parent container
width | float | Ti.UI.FILL | This property doesn't change the size of the actual switch but it's parent container
trackOnColor | String | n/a | Color for the track of the switch when it is positioned on `On`
trackOffColor | String | n/a | Color for the track of the switch when it is positioned on `Off` 
thumbOnColor | String | n/a | Color for the switch thumb when positioned to `On`
thumbOffColor | String | n/a | Color for the switch thumb when positioned to `Off`

### Events

- change

## MDProgress

To create a progressbar use the following code. 

```javascript
var pb = Material.createProgressBar({});
```

It accepts these properties:

### Properties

Property | Type | Default | Description
--- | --- | --- | ----
value | float | 0 | Determines the progress
width | float | Ti.UI.FILL | Sets the width of the progressbar
trackTintColor | String | `transparent` | Color for the track
tintColor | String | `transparent` | Color of the progress
radius | float | 50 | Radius of the circular progressbar
progressSyle | enum | 0 | 0 stands for **circular**, 1 is for **linear** progressbar
progressType | enum | 0 | 0 is for **indeterminate**, 1 is for **determinate**

### Events

n/a

## LICENSE

MIT.

