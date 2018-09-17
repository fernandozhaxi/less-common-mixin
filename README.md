# less-common-mixins

Less mixins often used.

## Content Table

- [Install](#install)
- [Import](#import)
- [Examples](#examples)
  - [background-gradient](#background-gradient)
  - [background-gradient-x](#background-gradient-x)
  - [background-gradient-y](#background-gradient-y)
  - [background-cover](#background-cover)
  - [background-contain](#background-contain)
  - [border-top-radius](#border-top-radius)
  - [border-right-radius](#border-right-radius)
  - [border-bottom-radius](#border-bottom-radius)
  - [border-left-radius](#border-left-radius)
  - [caret-up](#caret-up)
  - [caret-right](#caret-right)
  - [caret-down](#caret-down)
  - [caret-left](#caret-left)
  - [circle](#circle)
  - [clearfix](#clearfix)
  - [flex-center](#flex-center)
  - [hr](#hr)
  - [list-unstyle](#list-unstyle)
  - [rect](#rect)
  - [square](#square)
  - [text-truncate](#text-truncate)

## Install

```sh
npm install --save less-common-mixins
```

## Import

```less
@import 'less-common-mixins';
```

## Examples

### background-gradient

**Usage:**

```less
.background-gradient(@begin; @end; @angle: 180deg);
```

**Input:**

```less
.background-gradient-default {
  .background-gradient(#fff, #000);
}

.background-gradient-custom-angle {
  .background-gradient(#fff, #000, 60deg);
}
```

**Output:**

```css
.background-gradient-default {
  background-color: #808080;
  background-image: linear-gradient(180deg, #fff, #000);
}

.background-gradient-custom-angle {
  background-color: #808080;
  background-image: linear-gradient(60deg, #fff, #000);
}
```

### background-gradient-x

**Usage:**

```less
.background-gradient-x(@begin; @end);
```

**Input:**

```less
.background-gradient-x {
  .background-gradient-x(#fff, #000);
}
```

**Output:**

```css
.background-gradient-x {
  background-color: #808080;
  background-image: linear-gradient(90deg, #fff, #000);
}
```

### background-gradient-y

**Usage:**

```less
.background-gradient-y(@begin; @end);
```

**Input:**

```less
.background-gradient-y {
  .background-gradient-y(#fff, #000);
}
```

**Output:**

```css
.background-gradient-y {
  background-color: #808080;
  background-image: linear-gradient(180deg, #fff, #000);
}
```

### background-cover

**Usage:**

```less
.background-cover(@image);
```

**Input:**

```less
.background-cover {
  .background-cover('url(image)');
}
```

**Output:**

```css
.background-cover {
  background-image: 'url(image)';
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
}
```

### background-contain

**Usage:**

```less
.background-contain(@image);
```

**Input:**

```less
.background-contain {
  .background-contain('url(image)');
}
```

**Output:**

```css
.background-contain {
  background-image: 'url(image)';
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
}
```

### border-top-radius

**Usage:**

```less
.border-top-radius(@radius);
```

**Input:**

```less
.border-top-radius {
  .border-top-radius(10px);
}
```

**Output:**

```css
.border-top-radius {
  border-top-right-radius: 10px;
  border-top-left-radius: 10px;
}
```

### border-right-radius

**Usage:**

```less
.border-right-radius(@radius);
```

**Input:**

```less
.border-right-radius {
  .border-right-radius(10px);
}
```

**Output:**

```css
.border-right-radius {
  border-top-right-radius: 10px;
  border-botton-right-radius: 10px;
}
```

### border-bottom-radius

**Usage:**

```less
.border-bottom-radius(@radius);
```

**Input:**

```less
.border-bottom-radius {
  .border-bottom-radius(10px);
}
```

**Output:**

```css
.border-bottom-radius {
  border-bottom-right-radius: 10px;
  border-bottom-left-radius: 10px;
}
```

### border-left-radius

**Usage:**

```less
.border-left-radius(@radius);
```

**Input:**

```less
.border-left-radius {
  .border-left-radius(10px);
}
```

**Output:**

```css
.border-left-radius {
  border-top-left-radius: 10px;
  border-botton-left-radius: 10px;
}
```

### caret-up

**Usage:**

```less
.caret-up(@size; @color);
```

**Input:**

```less
.caret-up-default {
  .caret-up();
}

.caret-up-custom {
  .caret-up(12px, #000);
}
```

**Output:**

```css
.caret-up-default {
  border-top: 0;
  border-right: 8px solid transparent;
  border-bottom: 8px solid #666;
  border-left: 8px solid transparent;
}

.caret-up-custom {
  border-top: 0;
  border-right: 12px solid transparent;
  border-bottom: 12px solid #000;
  border-left: 12px solid transparent;
}
```

### caret-right

**Usage:**

```less
.caret-right(@size; @color);
```

**Input:**

```less
.caret-right-default {
  .caret-right();
}

.caret-right-custom {
  .caret-right(12px, #000);
}
```

**Output:**

```css
.caret-right-default {
  border-top: 8px solid transparent;
  border-right: 0;
  border-bottom: 8px solid transparent;
  border-left: 8px solid #666;
}

.caret-right-custom {
  border-top: 12px solid transparent;
  border-right: 0;
  border-bottom: 12px solid transparent;
  border-left: 12px solid #000;
}
```

### caret-down

**Usage:**

```less
.caret-down(@size; @color);
```

**Input:**

```less
.caret-down-default {
  .caret-down();
}

.caret-down-custom {
  .caret-down(12px, #000);
}
```

**Output:**

```css
.caret-down-default {
  border-top: 8px solid #666;
  border-right: 8px solid transparent;
  border-bottom: 0;
  border-left: 8px solid transparent;
}

.caret-down-custom {
  border-top: 12px solid #000;
  border-right: 12px solid transparent;
  border-bottom: 0;
  border-left: 12px solid transparent;
}
```

### caret-left

**Usage:**

```less
.caret-left(@size; @color);
```

**Input:**

```less
.caret-left-default {
  .caret-left();
}

.caret-left-custom {
  .caret-left(12px, #000);
}
```

**Output:**

```css
.caret-left-default {
  border-top: 8px solid transparent;
  border-right: 8px solid #666;
  border-bottom: 8px solid transparent;
  border-left: 0;
}

.caret-left-custom {
  border-top: 12px solid transparent;
  border-right: 12px solid #000;
  border-bottom: 12px solid transparent;
  border-left: 0;
}
```

### circle

**Usage:**

```less
.circle(@size);
```

**Input:**

```less
.circle {
  .circle(20px);
}
```

**Output:**

```css
.circle {
  width: 20px;
  height: 20px;
  border-radius: 50%;
}
```

### clearfix

**Usage:**

```less
.clearfix();
```

**Input:**

```less
.clearfix {
  .clearfix();
}
```

**Output:**

```css
.clearfix:after {
  display: table;
  clear: both;
  content: "";
}
```

### flex-center

**Usage:**

```less
.flex-center();
```

**Input:**

```less
.flex-center {
  .flex-center();
}
```

**Output:**

```css
.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

### hr

**Usage:**

```less
.hr(@color; @size: 1px; @style: solid; @direction: horizontal);
```

**Input:**

```less
.hr-default {
  .hr(#eee);
}

.hr-custom {
  .hr(#eee, 2px, dashed, vertical);
}
```

**Output:**

```css
.hr-default {
  width: 100%;
  border-top: 1px solid #eee;
}
.hr-custom {
  height: 100%;
  border-left: 2px dashed #eee;
}
```

### list-unstyle

**Usage:**

```less
.list-unstyle();
```

**Input:**

```less
.list-unstyle {
  .list-unstyle();
}
```

**Output:**

```css
.list-unstyle {
  padding-left: 0;
  list-style: none;
}
```

### rect

**Usage:**

```less
.rect(@width; @height);
```

**Input:**

```less
.rect {
  .rect(10px, 20px);
}
```

**Output:**

```css
.rect {
  width: 10px;
  height: 20px;
}
```

### square

**Usage:**

```less
.square(@size);
```

**Input:**

```less
.square {
  .square(10px);
}
```

**Output:**

```css
.square {
  width: 10px;
  height: 10px;
}
```

### text-truncate

**Usage:**

```less
.text-truncate(@rows: 1);
```

**Input:**

```less
.text-truncate-default {
  .text-truncate();
}

.text-truncate-custom {
  .text-truncate(3);
}
```

**Output:**

```css
.text-truncate-default {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.text-truncate-custom {
  display: -webkit-box;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-all;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
}
```

## License

MIT.
