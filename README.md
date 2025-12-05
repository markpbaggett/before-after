# Before-After Image Comparison Slider

A lightweight, dependency-free web component for creating before/after image comparison sliders.

Created as part of Texas A&M University's Sesquicentennial Celebration and heavily inspired by [twentytwenty](https://github.com/zurb/twentytwenty) and Knight Labs's [JuxtaposeJS](https://github.com/NUKnightLab/juxtapose)

## Features

- 🚀 Zero dependencies
- 📦 ~3KB minified
- 📱 Touch and mouse support
- ♿ Accessible
- 🎨 Customizable labels
- 🌐 Works everywhere (Web Components)
- 🔄 Horizontal and vertical orientations


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

You can load this as a pure web component but make sure you give it a height or it won't appear at all.

````

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
    start-position="50" 
    style="height: 600px;">
  </before-after>

  <script src="https://unpkg.com/@markpbaggett/before-after"></script>
</body>
</html>

```

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

## Attributes / Props

| Attribute        | Type     | Default      | Description                                    |
|------------------|----------|--------------|------------------------------------------------|
| `before`         | string   | required     | URL of the before image                        |
| `after`          | string   | required     | URL of the after image                         |
| `before-label`   | string   | "Before"     | Label for the before image                     |
| `after-label`    | string   | "After"      | Label for the after image                      |
| `start-position` | number   | 50           | Initial slider position (0–100)                |
| `show-labels`    | boolean  | true         | Show or hide labels                            |
| `orientation`    | string   | "horizontal" | Slider orientation: "horizontal" or "vertical" |


