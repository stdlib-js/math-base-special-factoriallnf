<!--

@license Apache-2.0

Copyright (c) 2025 The Stdlib Authors.

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


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# factoriallnf

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Natural logarithm of the [factorial][factorial-function] of a single-precision floating-point number.

<section class="intro">

The natural logarithm of the factorial function may be expressed

<!-- <equation class="equation" label="eq:factorialln_function" align="center" raw="f(n)=\ln (n!)" alt="Equation of the natural logarithm of the factorial."> -->

```math
f(n)=\ln (n!)
```

<!-- </equation> -->

The [factorial function][factorial-function] may be defined as the product

<!-- <equation class="equation" label="eq:factorial_function" align="center" raw="n! = \prod_{k=1}^n k" alt="Factorial function definition"> -->

```math
n! = \prod_{k=1}^n k
```

<!-- </equation> -->

or according to the recurrence relation

<!-- <equation class="equation" label="eq:factorial_recurrence_relation" align="center" raw="n! = \begin{cases}1 & \textrm{if } n = 0,\\(n-1)! \times n & \textrm{if } n > 1\end{cases}" alt="Factorial function recurrence relation"> -->

```math
n! = \begin{cases}1 & \textrm{if } n = 0,\\(n-1)! \times n & \textrm{if } n > 1\end{cases}
```

<!-- </equation> -->

Following the convention for an [empty product][empty-product], in all definitions,

<!-- <equation class="equation" label="eq:zero_factorial" align="center" raw="0! = 1" alt="Zero factorial"> -->

```math
0! = 1
```

<!-- </equation> -->

The [Gamma][gamma-function] function extends the [factorial function][factorial-function] for non-integer values.

<!-- <equation class="equation" label="eq:factorial_function_and_gamma" align="center" raw="n! = \Gamma(n+1)" alt="Factorial function extension via the Gamma function"> -->

```math
n! = \Gamma(n+1)
```

<!-- </equation> -->

The [factorial][factorial-function] of a **negative** integer is not defined.

Evaluating the natural logarithm of [factorial function][factorial-function] is useful as the [factorial function][factorial-function] can overflow for large `n`. Thus, `factoriallnf( n )` is generally preferred to `lnf( n! )`.

</section>

<!-- /.intro -->



<section class="usage">

## Usage

```javascript
import factoriallnf from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-factoriallnf@v0.1.1-deno/mod.js';
```

#### factoriallnf( x )

Evaluates the natural logarithm of the [factorial][factorial-function] of a single-precision floating-point number. For input values other than negative integers, the function returns `ln( x! ) = ln( Γ(x+1) )`, where `Γ` is the [Gamma][gamma-function] function. For negative integers, the function returns `NaN`.

```javascript
var v = factoriallnf( 3.0 );
// returns ~1.792

v = factoriallnf( 2.4 );
// returns ~1.092

v = factoriallnf( -1.0 );
// returns NaN

v = factoriallnf( -1.5 );
// returns ~1.266
```

If provided `NaN`, the function returns `NaN`.

```javascript
var v = factoriallnf( NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
import uniform from 'https://cdn.jsdelivr.net/gh/stdlib-js/random-array-uniform@deno/mod.js';
import logEachMap from 'https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each-map@deno/mod.js';
import factoriallnf from 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-factoriallnf@v0.1.1-deno/mod.js';

var opts = {
    'dtype': 'float32'
};
var x = uniform( 100, -10.0, 50.0, opts );

logEachMap( 'factoriallnf(%0.4f) = %0.4f', x, factoriallnf );
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-factoriallnf.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-factoriallnf

[test-image]: https://github.com/stdlib-js/math-base-special-factoriallnf/actions/workflows/test.yml/badge.svg?branch=v0.1.1
[test-url]: https://github.com/stdlib-js/math-base-special-factoriallnf/actions/workflows/test.yml?query=branch:v0.1.1

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-factoriallnf/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-factoriallnf?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-factoriallnf.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-factoriallnf/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-factoriallnf/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-factoriallnf/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-factoriallnf/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-factoriallnf/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-factoriallnf/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-factoriallnf/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-factoriallnf/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-factoriallnf/main/LICENSE

[gamma-function]: https://en.wikipedia.org/wiki/Gamma_Function

[factorial-function]: https://en.wikipedia.org/wiki/Factorial

[empty-product]: https://en.wikipedia.org/wiki/Empty_product

<!-- <related-links> -->

<!-- </related-links> -->

</section>

<!-- /.links -->
