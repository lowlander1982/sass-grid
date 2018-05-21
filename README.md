# Sass grid

A simple grid system built in scss

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Make sure you have a sass loader in your project

### Installing

Include the `styles/base.scss` file in your main scrit or build a CSS based on that file and add a reference of it in your HTML. (Or use webpack, gulp, grunt ...etc strategies to include it in your build package)

## How it works

This framework will enrich your HTML to allow you easier manage of your grid system.

This examples will help you understand how it works:

### The container

This is just the main wrapper, before that the grid won't work as expected

```
<!-- Makes the container full width -->
<div class="container-fluid">
</div>
```

```
<!-- Makes the container with a fixed width based on the breakpoints -->
<div class="container">
</div>
```

### The row

The first child of the container or of a column

```
<!-- The row will reset the margins to the gutter so the columns start as intended -->
<div class="row">
</div>
```

### The columns

The columns are based on a 12 column grid system and they are mobile first intended

```
<!-- This will render each column occupying all the width on mobile, half size on tablet, 1/3 of the space on desktop and 1/4 of space on large screens. The number on the column indicates how much columns of a 12 column grid system they occupy -->
<div class="row">
  <div class="col-xs-12 col-sm-6 col-md-4 col-lg-3">
    COL 1
  </div>
  <div class="col-xs-12 col-sm-6 col-md-4 col-lg-3">
    COL 2
  </div>
  <div class="col-xs-12 col-sm-6 col-md-4 col-lg-3">
    COL 3
  </div>
  <div class="col-xs-12 col-sm-6 col-md-4 col-lg-3">
    COL 4
  </div>
</div>
```

```
<!-- As this is mobile first, you can always define from small to big, like this example that occupies the entire width on mobile, bug half on the other breakpoints -->
<div class="row">
  <div class="col-xs-12 col-sm-6">
    COL 1
  </div>
  <div class="col-xs-12 col-sm-6">
    COL 2
  </div>
</div>
```

### mixins

You can always use a mixin wherever you want:

```
// This example defines the font size to be 20px from tablet and bigger breakpoints
@include do-breakpoint('md') {
  font-size: 20px;
}
```

Just remember this is mobile first and everything will be easier...

## Contributors

* **David Gomez Fonnegra** - *GRID work* - [lowlander1982](https://github.com/lowlander1982)
* **Sebastian Lopez** - *Fixes and refinings* - [SebPez](https://github.com/SebPez)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
