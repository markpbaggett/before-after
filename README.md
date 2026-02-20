# Before-After Image Comparison Slider

A lightweight, dependency-free web component library for comparing two images. Includes two components: a split-slider (`<before-after>`) and an opacity blender (`<opacity-compare>`).

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

---

## `<before-after>` — Split Slider

Reveals one image by dragging a dividing line horizontally or vertically across the frame.

```html
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

### Styling

```css
before-after {
  display: block;
  height: 600px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```

### Attributes

| Attribute        | Type     | Default      | Description                                    |
|------------------|----------|--------------|------------------------------------------------|
| `before`         | string   | required     | URL of the before image                        |
| `after`          | string   | required     | URL of the after image                         |
| `before-label`   | string   | "Before"     | Label for the before image                     |
| `after-label`    | string   | "After"      | Label for the after image                      |
| `start-position` | number   | 50           | Initial slider position (0–100)                |
| `show-labels`    | boolean  | true         | Show or hide labels                            |
| `orientation`    | string   | "horizontal" | Slider orientation: "horizontal" or "vertical" |
| `link-url`       | string   | optional     | Webpage to link branding to                    |
| `link-text`      | string   | optional     | Text to show in branding badge                 |
| `favicon-url`    | string   | optional     | Small image shown before branding text         |

---

## `<opacity-compare>` — Opacity Blender

Stacks two images on top of each other. A slider bar at the bottom of the component controls the opacity of the top image, letting you smoothly blend between them.

Drag the slider left to reveal the bottom (before) image; drag right to reveal the top (after) image.

```html
<!DOCTYPE html>
<html>
<head>
  <title>Opacity Compare Demo</title>
</head>
<body>
  <opacity-compare
    before="before.jpg"
    after="after.jpg"
    before-label="Before"
    after-label="After"
    start-opacity="50"
    style="height: 600px;">
  </opacity-compare>

  <script src="https://unpkg.com/@markpbaggett/before-after"></script>
</body>
</html>
```

### Styling

```css
opacity-compare {
  display: block;
  height: 600px;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```

### Attributes

| Attribute       | Type   | Default  | Description                                        |
|-----------------|--------|----------|----------------------------------------------------|
| `before`        | string | required | URL of the bottom image                            |
| `after`         | string | required | URL of the top image (opacity-controlled)          |
| `before-label`  | string | "Before" | Label for the bottom image                         |
| `after-label`   | string | "After"  | Label for the top image                            |
| `start-opacity` | number | 50       | Initial opacity of the top image (0–100)           |

### Keyboard Support

Both components are keyboard accessible. When the slider is focused:

| Key              | Action                  |
|------------------|-------------------------|
| `←` / `→`        | Move slider by 1%       |
| `Shift` + `←`/`→`| Move slider by 10%      |
| `Home`           | Jump to 0%              |
| `End`            | Jump to 100%            |


