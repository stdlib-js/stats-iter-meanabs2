<!--

@license Apache-2.0

Copyright (c) 2019 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->

# itermeanabs2

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the [arithmetic mean][arithmetic-mean] of squared absolute values for all [iterated][mdn-iterator-protocol] values.

<section class="intro">

The [arithmetic mean][arithmetic-mean] of squared absolute values is defined as

<!-- <equation class="equation" label="eq:arithmetic_mean_squared_absolute_values" align="center" raw="m = \frac{1}{n} \sum_{i=0}^{n-1} x_i^2" alt="Equation for the arithmetic mean of squared absolute values."> -->

<div class="equation" align="center" data-raw-text="m = \frac{1}{n} \sum_{i=0}^{n-1} x_i^2" data-equation="eq:arithmetic_mean_squared_absolute_values">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@d6537e6e0eb08987edeffda2d81b9a9197bdd7e0/lib/node_modules/@stdlib/stats/iter/meanabs2/docs/img/equation_arithmetic_mean_squared_absolute_values.svg" alt="Equation for the arithmetic mean of squared absolute values.">
    <br>
</div>

<!-- </equation> -->

</section>

<!-- /.intro -->

<!-- Package usage documentation. -->



<section class="usage">

## Usage

To use in Observable,

```javascript
itermeanabs2 = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-iter-meanabs2@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var itermeanabs2 = require( 'path/to/vendor/umd/stats-iter-meanabs2/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/stats-iter-meanabs2@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.itermeanabs2;
})();
</script>
```

#### itermeanabs2( iterator )

Computes the [arithmetic mean][arithmetic-mean] of squared absolute values for all [iterated][mdn-iterator-protocol] values.

```javascript
var array2iterator = require( '@stdlib/array-to-iterator' );

var arr = array2iterator( [ 1.0, -2.0, -3.0, 4.0 ] );

var m = itermeanabs2( arr );
// returns 7.5
```

</section>

<!-- /.usage -->

<!-- Package usage notes. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="notes">

## Notes

-   If an iterated value is non-numeric (including `NaN`), the returned [`iterator`][mdn-iterator-protocol] returns `NaN`. If non-numeric iterated values are possible, you are advised to provide an [`iterator`][mdn-iterator-protocol] which type checks and handles non-numeric values accordingly.

</section>

<!-- /.notes -->

<!-- Package usage examples. -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/random-iter-uniform@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/stats-iter-meanabs2@umd/browser.js"></script>
<script type="text/javascript">
(function () {

// Create an iterator for generating uniformly distributed pseudorandom numbers:
var rand = runif( -10.0, 10.0, {
    'seed': 1234,
    'iter': 100
});

// Compute the arithmetic mean of squared absolute values:
var m = itermeanabs2( rand );
// returns <number>

console.log( 'meanabs2: %d.', m );

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section to include cited references. If references are included, add a horizontal rule *before* the section. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="references">

</section>

<!-- /.references -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/stats/iter/mean`][@stdlib/stats/iter/mean]</span><span class="delimiter">: </span><span class="description">compute the arithmetic mean over all iterated values.</span>
-   <span class="package-name">[`@stdlib/stats/iter/meanabs`][@stdlib/stats/iter/meanabs]</span><span class="delimiter">: </span><span class="description">compute the arithmetic mean of absolute values for all iterated values.</span>
-   <span class="package-name">[`@stdlib/stats/iter/mmeanabs2`][@stdlib/stats/iter/mmeanabs2]</span><span class="delimiter">: </span><span class="description">create an iterator which iteratively computes a moving arithmetic mean of squared absolute values.</span>
-   <span class="package-name">[`@stdlib/stats/iter/sumabs2`][@stdlib/stats/iter/sumabs2]</span><span class="delimiter">: </span><span class="description">compute the sum of squared absolute values for all iterated values.</span>

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-iter-meanabs2.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-iter-meanabs2

[test-image]: https://github.com/stdlib-js/stats-iter-meanabs2/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/stats-iter-meanabs2/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-iter-meanabs2/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-iter-meanabs2?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-iter-meanabs2.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-iter-meanabs2/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-iter-meanabs2/tree/deno
[umd-url]: https://github.com/stdlib-js/stats-iter-meanabs2/tree/umd
[esm-url]: https://github.com/stdlib-js/stats-iter-meanabs2/tree/esm
[branches-url]: https://github.com/stdlib-js/stats-iter-meanabs2/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-iter-meanabs2/main/LICENSE

[arithmetic-mean]: https://en.wikipedia.org/wiki/Arithmetic_mean

[mdn-iterator-protocol]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols#The_iterator_protocol

<!-- <related-links> -->

[@stdlib/stats/iter/mean]: https://github.com/stdlib-js/stats-iter-mean/tree/umd

[@stdlib/stats/iter/meanabs]: https://github.com/stdlib-js/stats-iter-meanabs/tree/umd

[@stdlib/stats/iter/mmeanabs2]: https://github.com/stdlib-js/stats-iter-mmeanabs2/tree/umd

[@stdlib/stats/iter/sumabs2]: https://github.com/stdlib-js/stats-iter-sumabs2/tree/umd

<!-- </related-links> -->

</section>

<!-- /.links -->