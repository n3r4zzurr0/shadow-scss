[npm-image]: https://img.shields.io/npm/v/shadow-scss.svg
[npm-url]: https://npmjs.org/package/shadow-scss
[license-image]: https://img.shields.io/github/license/n3r4zzurr0/range-slider-input.svg
[license-url]: https://github.com/n3r4zzurr0/range-slider-input/blob/main/LICENSE

# shadow-scss
[![npm][npm-image]][npm-url] [![license][license-image]][license-url]

A set of two Sass functions (`box-shadow()` and `text-shadow()`) to write multiple shadows.

**[Examples](https://n3r4zzurr0.in/shadow-scss/)**

## Installation

With npm,
```
npm install shadow-scss
```
or just copy the content of the [`_shadow.scss`](https://raw.githubusercontent.com/n3r4zzurr0/shadow-scss/main/_shadow.scss) file into your Sass directory.

## Usage

With npm,
```
@import "shadow-scss";
```
or just `@import` the `_shadow.scss` partial into your Sass project.

**`box-shadow()`**

```scss
box-shadow: box-shadow(
  $color: #000,
  $step: 2px,
  $count: 10
)
```

**`text-shadow()`**

```scss
text-shadow: text-shadow(
  $color: #ccc,
  $stepX: -.5px,
  $stepY: .5px,
  $count: 50
)
```

## Options

For `$x`, `$y`, `$blur-radius`, `$spread-radius`, `$color`, `$step`, `$stepX` and `$stepY`, custom functions can also be passed through, when writing multiple shadows. These functions are called with 2 parameters (`$i` and `$count`) and can be defined as,

```scss
@function func-name($i, $count) {
  @return calc($i / $count) * 5px;
}
```

where `$i` denotes the nth shadow and `$count` is the total number of shadows which was initially defined.

<table>
<tr>
	<th>Parameter</th>
	<th><code>box-shadow()</code></th>
	<th><code>text-shadow()</code></th>
	<th>Default Value</th>
	<th>Description</th>
</tr>
<tr>
	<td><code>$inset</code></td>
	<td>&#x2611;</td>
	<td>&#x2612;</td>
	<td><code>false</code></td>
	<td>Boolean value that specifies if the <code>inset</code> keyword is to be included or not.</td>
</tr>
<tr>
	<td><code>$x</code></td>
	<td>&#x2611;</td>
	<td>&#x2611;</td>
	<td><code>0</code></td>
	<td>Number or Function that specifies the horizontal distance. </td>
</tr>
<tr>
	<td><code>$y</code></td>
	<td>&#x2611;</td>
	<td>&#x2611;</td>
	<td><code>0</code></td>
	<td>Number or Function that specifies the vertical distance. </td>
</tr>
<tr>
	<td><code>$blur-radius</code></td>
	<td>&#x2611;</td>
	<td>&#x2611;</td>
	<td><code>0</code></td>
	<td>Number or Function that specifies the blur amount.</td>
</tr>
<tr>
	<td><code>$spread-radius</code></td>
	<td>&#x2611;</td>
	<td>&#x2612;</td>
	<td><code>0</code></td>
	<td>Number or Function that specifies the spread amount.</td>
</tr>
<tr>
	<td><code>$color</code></td>
	<td>&#x2611;</td>
	<td>&#x2611;</td>
	<td><code>#000</code></td>
	<td>Color or Function that specifies the color.</td>
</tr>
<tr>
	<td><code>$step</code></td>
	<td>&#x2611;</td>
	<td>&#x2611;</td>
	<td><code>0</code></td>
	<td>Number or Function that specifies the horizontal and the vertical difference between the distances of the shadows.</td>
</tr>
<tr>
	<td><code>$stepX</code></td>
	<td>&#x2611;</td>
	<td>&#x2611;</td>
	<td><code>null</code></td>
	<td>Number or Function that specifies the horizontal difference between the distances of the shadows.<br/><br/>If its value is <code>null</code> (default), the value of <code>$step</code> is used.</td>
</tr>
<tr>
	<td><code>$stepY</code></td>
	<td>&#x2611;</td>
	<td>&#x2611;</td>
	<td><code>null</code></td>
	<td>Number or Function that specifies the vertical difference between the distances of the shadows.<br/><br/>If its value is <code>null</code> (default), the value of <code>$step</code> is used.</td>
</tr>
<tr>
	<td><code>$count</code></td>
	<td>&#x2611;</td>
	<td>&#x2611;</td>
	<td><code>1</code></td>
	<td>Number that specifies the number of shadows to be written.</td>
</tr>
</table>

<br/>

Refer to the MDN Web Docs for [`box-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow#values) and [`text-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow#values) for a better understanding of the native parameters.

## License

MIT © [Utkarsh Verma](https://github.com/n3r4zzurr0)
