# Material Color Palette Template

This is the resource of color values for Android.  
Reference : [Google Material Design Color Style](https://www.google.com/design/spec/style/color.html#color-color-palette)

![Preview](/art/preview.png)

## Usage

### Copy to values folder in your project.

[colors_material](/colors_material.xml)

![Usage](/art/usage.png)

### Reference

```xml
<resources>
    <style name="AppTheme" parent="android:Theme.Material.Light">
        <item name="android:colorPrimary">@color/material_indigo_500</item>
        <item name="android:colorPrimaryDark">@color/material_indigo_700</item>
        <item name="android:colorAccent">@color/material_deep_orange_500</item>
        <item name="android:textColorPrimary">@android:color/white</item>
    </style>
</resources>
```

## How to convert

I converted to style of colors in Android.
I used the macro in vim.

![Convert](/art/convert.gif)

### Step 1. Copy and paste

* Copy from [Color palette](https://www.google.com/design/spec/style/color.html#color-color-palette) and paste to vim

```
50#E3F2FD
100#BBDEFB
200#90CAF9
300#64B5F6
400#42A5F5
500#2196F3
600#1E88E5
700#1976D2
800#1565C0
900#0D47A1
A100#82B1FF
A200#448AFF
A400#2979FF
A700#2962FF
```

### Step 2. Register the macro 1 

* Register the macro that hex of color convert to lower case.

```
ql
0
f#
<ctrl-v>
14j
$
u
q
```

### Step 3. Register the macro 2 

* Register the macro adding the tag and value of alpha(ff).  

```
qt
I
<color name="material_blue_
<ESC>
f#
I
">
<ESC>
I
a
ff
<ESC>
A
<ESC>
j
q
```

### Step 4. Use the above macros

```
14@l
14@t
```
