# Before-After Image Comparison Slider

A lightweight, dependency-free web component for creating before/after image comparison sliders.

Created as part of Texas A&M University's Sesquicentennial Celebration and heavily inspired by Zurb's Twenty / Twenty and Knight Labs's Juxtaposition.js.

## Features

- 🚀 Zero dependencies
- 📦 ~3KB minified
- 📱 Touch and mouse support
- ♿ Accessible
- 🎨 Customizable labels
- 🌐 Works everywhere (Web Components)

## Installation

### Via unpkg
```html
<script src="https://unpkg.com/@markpbaggett/before-after"></script>
```

### Via jsDelivr

```html
<script src="https://cdn.jsdelivr.net/npm/@markpbaggett/before-after"></script>
```

### Via npm

```shell
npm install @markpbaggett/before-after
```

## Usage

<!DOCTYPE html>
<html>
<head>
  <title>Before/After Demo</title>
</head>
<body>
  <before-after 
    before="before.jpg" 
    after="after.jpg"
    before-label="Label that Goes with Before"
    after-label="Label that Goes with After"
    start-position="50" # where do you want the bar to start
    style="height: 600px;"> # make sure to set height or viewer won't appear
  </before-after>

  <script src="https://unpkg.com/@markpbaggett/before-after"></script>
</body>
</html>

## Styling

Use custom properties for easy theming like:

```css
before-after {
  display: block;
  height: 600px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```
