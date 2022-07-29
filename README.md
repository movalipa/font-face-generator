# Font Face Generator
An automatic @font-face generator powered by Sass

# Setup
Setup in 4 simple steps

## Step 1 (Copy)
Copy the `sample.scss` and paste It into the root directory including font files.

## Step 2 (Rename)
Rename `sample.scss` into `fontName.scss`

## step 3 (Config)
Open `fontName.scss` and scroll down for `config`, and type your font pack details in variables
```scss
// Config
$name: "FontName";
$dir: "./";
$weights: "Thin", "ExtraLight", "Light", "Regular", "Medium", "SemiBold",
  "Bold", "ExtraBold", "Black";
$italic: false;
$file_types: "ttf";
```

### $name
- Font's Name
- Expected values: *PascalCase* e.g. `"Roboto"`, `"Inter"`

### $dir
- Font files directory path
- Expected values: Existent File Path(If font files placed in root, use `"./"`)

### $weights
- Available font Weights
- Expected values: *PascalCase* `"Thin"`, `"ExtraLight"`, `"Light"`, `"Regular"`, `"Medium"`, `"SemiBold"`, `"Bold"`, `"ExtraBold"`, `"Black"`

### $italic
- If *Italic* style available `true` otherwise `false`
- Expected values: *lowercase* `true` or `false`

### $file_types
- Available file type extentions(It can be more than one)
- Expected values: *lowercase* `"woff"`, `"woff2"`, `"ttf"`, `"otf"`, `"eot"`, `"svg"`

## Step 4 (Run)
Run `fontName.scss`

Don't know how to run SASS file [Here](https://sass-lang.com/install).

If you are using `VSCode`, you can also use [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=ritwickdey.live-sass) extention.

# Samples
In this repository I already prepared two font packs for you

## Roboto
### Config
```scss
// Config
$name: "Roboto";
$dir: "./";
$weights: "Thin", "Light", "Regular", "Medium", "Bold", "Black";
$italic: true;
$file_types: "ttf";
```
### CSS output
```css
/* Auto Generated @font-face */
/* ----- Roboto ----- */
/* Available Weights : 100 300 400 500 700 900 */
/* Italic Included */
@font-face {
  font-family: "Roboto";
  src: local("Roboto"), local("Roboto-Thin"), url("./Roboto-Thin.ttf") format("truetype");
  font-weight: 100;
  font-style: normal;
}
@font-face {
  font-family: "Roboto";
  src: local("Roboto"), local("Roboto-ThinItalic"), url("./Roboto-ThinItalic.ttf") format("truetype");
  font-weight: 100;
  font-style: italic;
}
@font-face {
  font-family: "Roboto";
  src: local("Roboto"), local("Roboto-Light"), url("./Roboto-Light.ttf") format("truetype");
  font-weight: 300;
  font-style: normal;
}
@font-face {
  font-family: "Roboto";
  src: local("Roboto"), local("Roboto-LightItalic"), url("./Roboto-LightItalic.ttf") format("truetype");
  font-weight: 300;
  font-style: italic;
}
.
.
.
```

## Inter
### Config
```scss
// Config
$name: "Inter";
$dir: "./";
$weights: "Thin", "ExtraLight", "Light", "Regular", "Medium", "SemiBold", "Bold", "ExtraBold", "Black";
$italic: false;
$file_types: "ttf";
```
### CSS output
```css
/* Auto Generated @font-face */
/* ----- Inter ----- */
/* Available Weights : 100 200 300 400 500 600 700 800 900 */
/* Italic NOT Included */
@font-face {
  font-family: "Inter";
  src: local("Inter"), local("Inter-Thin"), url("./Inter-Thin.ttf") format("truetype");
  font-weight: 100;
  font-style: normal;
}
@font-face {
  font-family: "Inter";
  src: local("Inter"), local("Inter-ExtraLight"), url("./Inter-ExtraLight.ttf") format("truetype");
  font-weight: 200;
  font-style: normal;
}
@font-face {
  font-family: "Inter";
  src: local("Inter"), local("Inter-Light"), url("./Inter-Light.ttf") format("truetype");
  font-weight: 300;
  font-style: normal;
}
@font-face {
  font-family: "Inter";
  src: local("Inter"), local("Inter-Regular"), url("./Inter-Regular.ttf") format("truetype");
  font-weight: 400;
  font-style: normal;
}
.
.
.
```