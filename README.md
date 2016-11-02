# Polymer Plot Components

A highly modular and configurable symbolic plotter for Polymer. Plotting analytic functions in HTML has never been so easy thanks to SVG, Math.js and D3.js. You may see Polymer as the glue that makes plotting this easy.

#### Wait there, why this in the first place if Google Chart already exists as a Polymer Component?

This is **not** the same as Google Charts. Google Charts is used for plotting **numerical data** in a lot of fashions, Polymer Plot Components is a tool for plotting **symbolical data** as curves.

You usually use Google Charts to plot `[1, 1.05, 0.8, 1.25]`. On the other hand, you use Polymer Plot Components for plotting `x^3` or any formula you want, in any range you want, in any resolution you want, without having to make sample data for each function you want to plot.

## Installation

Install via Bower:

```
bower install --save polymer-plot-components
```

## Usage

Add the collection of components to your document or application:

### What should I include in my app?

```html
<link rel="import" href="bower_components/polymer-plot-components/plot-components.html">
```

### Example

Put this inside anywhere in your document body. You should expect the result to be a `inline-block` component.

```html
<plot-canvas>
  <plot-title>Example Graphic</plot-title>

  <!-- Set a plot area with your own range and dimensions in pixels -->
  <plot-area width="500" height="200" xmin="0" xmax="10">
    <!-- Draw axis as you wish -->
    <plot-x-axis></plot-x-axis>

    <!-- Group lines in the same axis -->
    <plot-y-axis ymin="-1" ymax="1">
      <!-- Each line is easily customizable -->
      <plot-line formula="(0.1*x)^2" line-color="red"></plot-line>
      <plot-line formula="sin(x)" line-color="green"></plot-line>
    </plot-y-axis>
  </plot-area>

  <!-- Break the line for a subplot -->
  <br/>

  <!-- Stack them as you wish. Subplotting is easy -->
  <plot-area width="230" height="200" xmin="-1" xmax="1">
    <plot-x-axis></plot-x-axis>
    <plot-y-axis ymin="-1" ymax="1">
      <plot-line formula="x^3" line-color="orange"></plot-line>
    </plot-y-axis>
  </plot-area>

  <plot-area width="230" height="200" xmin="0" xmax="1">
    <plot-x-axis></plot-x-axis>
    <plot-y-axis ymin="0" ymax="1">
      <plot-line formula="sqrt(x)" line-color="blue"></plot-line>
      <plot-line formula="x^2" line-color="red"></plot-line>
    </plot-y-axis>
  </plot-area>
</plot-canvas>
```

## Component reference

A description for using one of each component is described here. ***In construction!***

### plot-canvas
### plot-title
### plot-area
### plot-x-axis
### plot-y-axis
### plot-line

## License

BSD License. Check LICENSE.md for more information.

## Contribute

This is yet a purely academical excercise for a college course at Pontifical Catholic University of Chile. More configuration options should be required to have a functional product in a large group of situations.

As we get more experience with Polymer, this could be upgraded and maybe create a fully functional library in the future :).

Feel free to contribute by creating your own branches and pull requests.
