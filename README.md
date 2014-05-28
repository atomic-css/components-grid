# Atomic components: grid

CSS Grid component. The grid makes use of flex layout.

N.B. This component relies on particular dimensions being applied to cells in
the grid via other classes. For example,
[Atomic utils: dimension](https://github.com/atomic-css/utils-dimension).
If you need to align the cells, see
[Atomic utils: alignment](https://github.com/atomic-css/utils-alignment).

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
* `Grid--row` - flow the cells in row direction
* `Grid--column` - flow the cells in column direction
* `Grid-cell` - child class representing a unit

## Extensions

### `grid.layout.css`

Layout modifiers for `Grid`.

* `Grid--auto` - make all cells content-sized
* `Grid--equalWidth` - make all cells equal width
* `Grid--equalHeight` - make all cells equal height
* `Grid--2col` - split into 2 columns
* `Grid--3col` - split into 3 columns
* `Grid--4col` - split into 4 columns

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

* Flexible layout.
* Intelligent cell wrapping.
* Horizontal and vertical centering of cells.
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

## Browser support

* Google Chrome (latest)
* Opera (latest)
* Firefox (latest)
* Safari (latest)
* Internet Explorer 10+