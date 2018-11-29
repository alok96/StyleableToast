# StyleableToast
[![](https://img.shields.io/badge/API-16%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=16#l16)
[![APK](https://img.shields.io/badge/Download-Demo-brightgreen.svg)](https://github.com/Muddz/StyleableToast/raw/master/demo.apk)

An Android library that takes the standard toast to the next level with many styling options. Style your toasts either by code or with a style in `styles.xml`.
## Cases:

<img src="https://github.com/Muddz/StyleableToast/blob/master/cases.png" width="75%">


## Example with a style

1) Define a style in `styles.xml`. All available attributes:
```xml
    <style name="mytoast">
        <item name="stTextBold">true</item>
        <item name="stTextColor">#fff</item>
        <item name="stFont">@font/retrofont</item>
        <item name="stTextSize">14sp</item>
        <item name="stColorBackground">#fff</item>
        <item name="stSolidBackground">true</item>
        <item name="stStrokeWidth">3dp</item>
        <item name="stStrokeColor">#fff</item>
        <item name="stIconStart">@drawable/ic</item>
        <item name="stIconEnd">@drawable/ic</item>
        <item name="stLength">LONG</item> LONG or SHORT
        <item name="stGravity">top</item> top or center
        <item name="stRadius">5dp</item>
    </style>

```

2) Pass your style in the static constructor and call `show();`

```java
    StyleableToast.makeText(context, "Hello World!", Toast.LENGTH_LONG, R.style.mytoast).show();
```

## Example with builder pattern
```java
        new StyleableToast
                .Builder(context)
                .text("Hello world!")
                .textColor(Color.WHITE)
                .backgroundColor(Color.BLUE)
                .show();
```

    
## Installation

Add the dependency in your `build.gradle`
```groovy
dependencies {
    implementation 'com.muddzdev:styleabletoast:2.2.0'   
}
