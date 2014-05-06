# Atomic components: grid

CSS Grid component. The grid makes use of `inline-block` and
`box-sizing` to provide features that float-based layouts cannot.

N.B. This component relies on particular dimensions being applied to cells in
the grid via other classes. For example,
[Atomic utils: dimension](https://github.com/atomic-css/utils-dimension).
If you need gutter between cells, see
[Atomic utils: space](https://github.com/atomic-css/utils-space).

Read more about [Atomic framework](https://github.com/atomic-css/atomic).

## Installation

* [__Bower:__](http://bower.io)
  `bower install --save atomic-css-components-grid`
* __Download:__
  [zip](https://github.com/atomic-css/components-grid/zipball/master),
  [tar.gz](https://github.com/atomic-css/components-grid/tarball/master)
* __Git:__ `git clone https://github.com/atomic-css/components-grid.git`

## Available classes

* `Grid` - core grid component
* `Grid--fit` - make all grid units shrink wrap their content
* `Grid-cell` - child class representing a unit
* `Grid-cell--fit` - make one unit shrink wrap its content

## Extensions

### `grid.layout.css`

Layout modifiers for `Grid`.

* `Grid--2col` - split into 2 columns
* `Grid--3col` - split into 3 columns

### `grid.gutter.css`

Modifiers for creating gutter between grid cells.

* `Grid--gutter<O><Size>` - gutter of `<Size>` size in `<O>` orientation

Where orientation `<O>` can be:

* `A` - all
* `H` - horizontal
* `V` - vertical

and size `<Size>` can be:

* Small (5px)
* Medium (10px)
* Large (20px)

## Features

* Fluid layout.
* Intelligent cell wrapping.
* Horizontal centering of cells.
* Custom vertical alignment of cells (top, bottom, or middle).
* Cell width is controlled independently of grid gutter.
* Infinite nesting.
* Built-in redundancy.

## Usage

A simple grid is easy to create. A grid container can have any number of cells.
Each cell can be directly or indirectly styled to control their width and
alignment.

```html
<div class="Grid">
  <div class="Grid-cell u-size1of2">{…}</div>
  <div class="Grid-cell u-size1of2">{…}</div>
  <div class="Grid-cell u-size1of3">{…}</div>
  <div class="Grid-cell u-size1of3">{…}</div>
</div>
```

All cells within a grid can be centered by adding the `Grid--center` class to
the grid container:

```html
<div class="Grid Grid--center">
  <div class="Grid-cell u-size1of3">{…}</div>
  <div class="Grid-cell u-size1of3">{…}</div>
</div>
```

Or individual cells can be centered on their own line by adding the
`Grid-cell--center` class to a cell:

```html
<div class="Grid">
  <div class="Grid-cell u-size1of2">{…}</div>
  <div class="Grid-cell u-size1of2">{…}</div>
  <div class="Grid-cell Grid-cell--center u-size3of4">{…}</div>
</div>
```

To create a collection of items with arbitrary width, add the `Grid--fit` class
to the grid container. This way, we can still control each cell's width or
vertical alignment.

```html
<div class="Grid Grid--fit">
  <div class="Grid-cell">
    <div class="ProductThumbnail">
      {…}
    </div>
  </div>
  <div class="Grid-cell">
    <div class="ProductThumbnail">
      {…}
    </div>
  </div>
  <div class="Grid-cell">
    <div class="ProductThumbnail">
      {…}
    </div>
  </div>
</div>
```

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox 4+
* Safari 5+
* Internet Explorer 9+ (IE 8 needs to replace CSS `rem` units with `px`)