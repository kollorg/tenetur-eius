<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# Iterators

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Iterator utilities.

<section class="installation">

## Installation

```bash
npm install @kollorg/tenetur-eius
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm`][esm-url] branch (see [README][esm-readme]).
-   If you are using Deno, visit the [`deno`][deno-url] branch (see [README][deno-readme] for usage intructions).
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd`][umd-url] branch (see [README][umd-readme]).

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

To view installation and usage instructions specific to each branch build, be sure to explicitly navigate to the respective README files on each branch, as linked to above.

</section>

<section class="usage">

## Usage

```javascript
var ns = require( '@kollorg/tenetur-eius' );
```

#### ns

Namespace containing iterator utilities.

```javascript
var objectKeys = require( '@stdlib/utils/keys' );

var keys = objectKeys( ns );
// e.g., returns [ 'iterAny', 'iterAnyBy', ... ]
```

<!-- <toc pattern="*"> -->

<div class="namespace-toc">

-   <span class="signature">[`iterAdvance( iterator[, n] )`][@kollorg/tenetur-eius/advance]</span><span class="delimiter">: </span><span class="description">advance an iterator.</span>
-   <span class="signature">[`iterAnyBy( iterator, predicate[, thisArg] )`][@kollorg/tenetur-eius/any-by]</span><span class="delimiter">: </span><span class="description">test whether at least one iterated value passes a test implemented by a predicate function.</span>
-   <span class="signature">[`iterAny( iterator )`][@kollorg/tenetur-eius/any]</span><span class="delimiter">: </span><span class="description">test whether at least one iterated value is truthy.</span>
-   <span class="signature">[`iterConcat( iter0, ...iterator )`][@kollorg/tenetur-eius/concat]</span><span class="delimiter">: </span><span class="description">create an iterator which iterates over the values of two or more iterators.</span>
-   <span class="signature">[`iterConstant( value[, options] )`][@kollorg/tenetur-eius/constant]</span><span class="delimiter">: </span><span class="description">create an iterator which always returns the same value.</span>
-   <span class="signature">[`iterCounter( iterator )`][@kollorg/tenetur-eius/counter]</span><span class="delimiter">: </span><span class="description">create an iterator which iteratively computes the number of iterated values.</span>
-   <span class="signature">[`iterDatespace( start, stop[, N][, options] )`][@kollorg/tenetur-eius/datespace]</span><span class="delimiter">: </span><span class="description">create an iterator which returns evenly spaced dates over a specified interval.</span>
-   <span class="signature">[`iterDedupeBy( iterator, [limit,] fcn )`][@kollorg/tenetur-eius/dedupe-by]</span><span class="delimiter">: </span><span class="description">create an iterator which removes consecutive values that resolve to the same value according to a provided function.</span>
-   <span class="signature">[`iterDedupe( iterator[, limit] )`][@kollorg/tenetur-eius/dedupe]</span><span class="delimiter">: </span><span class="description">create an iterator which removes consecutive duplicated values.</span>
-   <span class="signature">[`iterEmpty()`][@kollorg/tenetur-eius/empty]</span><span class="delimiter">: </span><span class="description">create an empty iterator.</span>
-   <span class="signature">[`iterEveryBy( iterator, predicate[, thisArg] )`][@kollorg/tenetur-eius/every-by]</span><span class="delimiter">: </span><span class="description">test whether every iterated value passes a test implemented by a predicate function.</span>
-   <span class="signature">[`iterEvery( iterator )`][@kollorg/tenetur-eius/every]</span><span class="delimiter">: </span><span class="description">test whether all iterated values are truthy.</span>
-   <span class="signature">[`iterFill( iterator, value[, begin[, end]] )`][@kollorg/tenetur-eius/fill]</span><span class="delimiter">: </span><span class="description">create an iterator which replaces all values from a provided iterator from a start index to an end index with a static value.</span>
-   <span class="signature">[`iterFilterMap( iterator, fcn[, thisArg] )`][@kollorg/tenetur-eius/filter-map]</span><span class="delimiter">: </span><span class="description">create an iterator which both filters and maps the values of another iterator.</span>
-   <span class="signature">[`iterFilter( iterator, predicate[, thisArg] )`][@kollorg/tenetur-eius/filter]</span><span class="delimiter">: </span><span class="description">create an iterator which filters the values of another iterator according to a predicate function.</span>
-   <span class="signature">[`iterFirst( iterator )`][@kollorg/tenetur-eius/first]</span><span class="delimiter">: </span><span class="description">return the first iterated value.</span>
-   <span class="signature">[`iterFlow( methods )`][@kollorg/tenetur-eius/flow]</span><span class="delimiter">: </span><span class="description">create a fluent interface for chaining together iterator methods.</span>
-   <span class="signature">[`iterForEach( iterator, fcn[, thisArg] )`][@kollorg/tenetur-eius/for-each]</span><span class="delimiter">: </span><span class="description">create an iterator which invokes a function for each iterated value before returning the iterated value.</span>
-   <span class="signature">[`iterHead( iterator, n )`][@kollorg/tenetur-eius/head]</span><span class="delimiter">: </span><span class="description">create an iterator which returns the first `n` values of a provided iterator.</span>
-   <span class="signature">[`iterIncrspace( start, stop[, increment] )`][@kollorg/tenetur-eius/incrspace]</span><span class="delimiter">: </span><span class="description">create an iterator which returns evenly spaced numbers according to a specified increment.</span>
-   <span class="signature">[`iterIntersectionByHash( iter0, ...iterator, hashFcn[, thisArg] )`][@kollorg/tenetur-eius/intersection-by-hash]</span><span class="delimiter">: </span><span class="description">create an iterator which returns the intersection of two or more iterators according to a hash function.</span>
-   <span class="signature">[`iterIntersection( iter0, ...iterator )`][@kollorg/tenetur-eius/intersection]</span><span class="delimiter">: </span><span class="description">create an iterator which returns the intersection of two or more iterators.</span>
-   <span class="signature">[`iterLast( iterator )`][@kollorg/tenetur-eius/last]</span><span class="delimiter">: </span><span class="description">consume an entire iterator and return the last iterated value.</span>
-   <span class="signature">[`iterLength( iterator )`][@kollorg/tenetur-eius/length]</span><span class="delimiter">: </span><span class="description">return an iterator's length.</span>
-   <span class="signature">[`iterLinspace( start, stop[, N] )`][@kollorg/tenetur-eius/linspace]</span><span class="delimiter">: </span><span class="description">create an iterator which returns evenly spaced numbers over a specified interval.</span>
-   <span class="signature">[`iterLogspace( start, stop[, N][, options] )`][@kollorg/tenetur-eius/logspace]</span><span class="delimiter">: </span><span class="description">create an iterator which returns evenly spaced numbers over a specified interval.</span>
-   <span class="signature">[`iterMap( iterator, fcn[, thisArg] )`][@kollorg/tenetur-eius/map]</span><span class="delimiter">: </span><span class="description">create an iterator which invokes a function for each iterated value.</span>
-   <span class="signature">[`iterMapN( iter0, ...iterator, fcn[, thisArg] )`][@kollorg/tenetur-eius/mapn]</span><span class="delimiter">: </span><span class="description">create an iterator which transforms iterated values from two or more iterators by applying the iterated values as arguments to a provided function.</span>
-   <span class="signature">[`iterNoneBy( iterator, predicate[, thisArg] )`][@kollorg/tenetur-eius/none-by]</span><span class="delimiter">: </span><span class="description">test whether every iterated value fails a test implemented by a predicate function.</span>
-   <span class="signature">[`iterNone( iterator )`][@kollorg/tenetur-eius/none]</span><span class="delimiter">: </span><span class="description">test whether all iterated values are falsy.</span>
-   <span class="signature">[`iterNth( iterator, n )`][@kollorg/tenetur-eius/nth]</span><span class="delimiter">: </span><span class="description">return the nth iterated value.</span>
-   <span class="signature">[`iterThunk( iterFcn[, ...args] )`][@kollorg/tenetur-eius/pipeline-thunk]</span><span class="delimiter">: </span><span class="description">create an iterator "thunk".</span>
-   <span class="signature">[`iterPipeline( iterFcn0[, ...iterFcn] )`][@kollorg/tenetur-eius/pipeline]</span><span class="delimiter">: </span><span class="description">create an iterator pipeline.</span>
-   <span class="signature">[`iterPop( iterator[, clbk[, thisArg]] )`][@kollorg/tenetur-eius/pop]</span><span class="delimiter">: </span><span class="description">create an iterator which skips the last value of a provided iterator.</span>
-   <span class="signature">[`iterPush( iterator, ...items )`][@kollorg/tenetur-eius/push]</span><span class="delimiter">: </span><span class="description">create an iterator which appends additional values to the end of a provided iterator.</span>
-   <span class="signature">[`iterReject( iterator, predicate[, thisArg] )`][@kollorg/tenetur-eius/reject]</span><span class="delimiter">: </span><span class="description">create an iterator which rejects the values of another iterator according to a predicate function.</span>
-   <span class="signature">[`iterReplicateBy( iterator, fcn[, thisArg] )`][@kollorg/tenetur-eius/replicate-by]</span><span class="delimiter">: </span><span class="description">create an iterator which replicates each iterated value according to a provided function.</span>
-   <span class="signature">[`iterReplicate( iterator, n )`][@kollorg/tenetur-eius/replicate]</span><span class="delimiter">: </span><span class="description">create an iterator which replicates each iterated value a specified number of times.</span>
-   <span class="signature">[`iterShift( iterator[, clbk[, thisArg]] )`][@kollorg/tenetur-eius/shift]</span><span class="delimiter">: </span><span class="description">create an iterator which skips the first value of a provided iterator.</span>
-   <span class="signature">[`iterSlice( iterator[, begin[, end]] )`][@kollorg/tenetur-eius/slice]</span><span class="delimiter">: </span><span class="description">create an iterator which returns a subsequence of iterated values from a provided iterator.</span>
-   <span class="signature">[`iterSomeBy( iterator, n, predicate[, thisArg] )`][@kollorg/tenetur-eius/some-by]</span><span class="delimiter">: </span><span class="description">test whether at least `n` iterated values pass a test implemented by a predicate function.</span>
-   <span class="signature">[`iterSome( iterator, n )`][@kollorg/tenetur-eius/some]</span><span class="delimiter">: </span><span class="description">test whether at least `n` iterated values are truthy.</span>
-   <span class="signature">[`iterStep( start, increment[, N] )`][@kollorg/tenetur-eius/step]</span><span class="delimiter">: </span><span class="description">create an iterator which returns a sequence of numbers according to a specified increment.</span>
-   <span class="signature">[`iterStridedBy( iterator, fcn[, offset[, eager]][, thisArg] )`][@kollorg/tenetur-eius/strided-by]</span><span class="delimiter">: </span><span class="description">create an iterator which steps according to a provided callback function.</span>
-   <span class="signature">[`iterStrided( iterator, stride[, offset[, eager]] )`][@kollorg/tenetur-eius/strided]</span><span class="delimiter">: </span><span class="description">create an iterator which steps by a specified amount.</span>
-   <span class="signature">[`iterator2arrayviewRight( iterator, dest[, begin[, end]][, mapFcn[, thisArg]] )`][@kollorg/tenetur-eius/to-array-view-right]</span><span class="delimiter">: </span><span class="description">fill an array-like object view from right to left with values returned from an iterator.</span>
-   <span class="signature">[`iterator2arrayview( iterator, dest[, begin[, end]][, mapFcn[, thisArg]] )`][@kollorg/tenetur-eius/to-array-view]</span><span class="delimiter">: </span><span class="description">fill an array-like object view with values returned from an iterator.</span>
-   <span class="signature">[`iterUnion( iter0, ...iterator )`][@kollorg/tenetur-eius/union]</span><span class="delimiter">: </span><span class="description">create an iterator which returns the union of two or more iterators.</span>
-   <span class="signature">[`iterUniqueByHash( iterator, hashFcn[, thisArg] )`][@kollorg/tenetur-eius/unique-by-hash]</span><span class="delimiter">: </span><span class="description">create an iterator which returns unique values according to a hash function.</span>
-   <span class="signature">[`iterUniqueBy( iterator, predicate[, thisArg] )`][@kollorg/tenetur-eius/unique-by]</span><span class="delimiter">: </span><span class="description">create an iterator which returns unique values according to a predicate function.</span>
-   <span class="signature">[`iterUnique( iterator )`][@kollorg/tenetur-eius/unique]</span><span class="delimiter">: </span><span class="description">create an iterator which returns unique values.</span>
-   <span class="signature">[`iterUnitspace( start[, stop] )`][@kollorg/tenetur-eius/unitspace]</span><span class="delimiter">: </span><span class="description">create an iterator which returns numbers incremented by `1`.</span>
-   <span class="signature">[`iterUnshift( iterator, ...items )`][@kollorg/tenetur-eius/unshift]</span><span class="delimiter">: </span><span class="description">create an iterator which prepends values to the beginning of a provided iterator.</span>
-   <span class="signature">[`whileEach( iterator, predicate, fcn[, thisArg] )`][@kollorg/tenetur-eius/while-each]</span><span class="delimiter">: </span><span class="description">create an iterator which, while a test condition is true, invokes a function for each iterated value before returning the iterated value.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var objectKeys = require( '@stdlib/utils/keys' );
var uncapitalize = require( '@stdlib/string/uncapitalize' );
var replace = require( '@stdlib/string/replace' );
var contains = require( '@stdlib/assert/contains' );
var randu = require( '@stdlib/random/iter/randu' );
var ns = require( '@kollorg/tenetur-eius' );

// Create a fluent interface for chaining together iterator operations...

// Retrieve all the iterator utility names:
var keys = objectKeys( ns );

// Define a list of utilities to exclude from the fluent API:
var exclude = [ 'iterFlow', 'iterPipeline', 'iterThunk' ];

// Map each utility name to a fluent interface method...
var methods = {};
var key;
var k;
var i;
for ( i = 0; i < keys.length; i++ ) {
    key = keys[ i ];
    if ( contains( exclude, key ) ) {
        continue;
    }
    k = uncapitalize( replace( key, /^iter/, '' ) );
    methods[ k ] = ns[ key ];
}

// Create a fluent interface:
var FluentIterator = ns.iterFlow( methods );

// Create a new fluent interface iterator:
var it1 = new FluentIterator( randu() );

// Define a predicate function for filtering values:
function predicate( v ) {
    return ( v > 0.25 && v < 0.75 );
}

// Define a function which transforms iterated values:
function transform( v ) {
    return v * 10.0;
}

// Define a function to be invoked for each iterated value:
function log( v ) {
    console.log( v );
}

// Chain together a sequence of operations:
var it2 = it1.filter( predicate )
    .map( transform )
    .head( 10 )
    .forEach( log );

// Perform manual iteration...
var v;
while ( true ) {
    v = it2.next();
    if ( v.done ) {
        break;
    }
}
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

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

Copyright &copy; 2016-2024. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@kollorg/tenetur-eius.svg
[npm-url]: https://npmjs.org/package/@kollorg/tenetur-eius

[test-image]: https://github.com/kollorg/tenetur-eius/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/kollorg/tenetur-eius/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/kollorg/tenetur-eius/main.svg
[coverage-url]: https://codecov.io/github/kollorg/tenetur-eius?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/kollorg/tenetur-eius.svg
[dependencies-url]: https://david-dm.org/kollorg/tenetur-eius/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://app.gitter.im/#/room/#stdlib-js_stdlib:gitter.im

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/kollorg/tenetur-eius/tree/deno
[deno-readme]: https://github.com/kollorg/tenetur-eius/blob/deno/README.md
[umd-url]: https://github.com/kollorg/tenetur-eius/tree/umd
[umd-readme]: https://github.com/kollorg/tenetur-eius/blob/umd/README.md
[esm-url]: https://github.com/kollorg/tenetur-eius/tree/esm
[esm-readme]: https://github.com/kollorg/tenetur-eius/blob/esm/README.md
[branches-url]: https://github.com/kollorg/tenetur-eius/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/kollorg/tenetur-eius/main/LICENSE

<!-- <toc-links> -->

[@kollorg/tenetur-eius/advance]: https://github.com/kollorg/tenetur-eius/tree/main/advance

[@kollorg/tenetur-eius/any-by]: https://github.com/kollorg/tenetur-eius/tree/main/any-by

[@kollorg/tenetur-eius/any]: https://github.com/kollorg/tenetur-eius/tree/main/any

[@kollorg/tenetur-eius/concat]: https://github.com/kollorg/tenetur-eius/tree/main/concat

[@kollorg/tenetur-eius/constant]: https://github.com/kollorg/tenetur-eius/tree/main/constant

[@kollorg/tenetur-eius/counter]: https://github.com/kollorg/tenetur-eius/tree/main/counter

[@kollorg/tenetur-eius/datespace]: https://github.com/kollorg/tenetur-eius/tree/main/datespace

[@kollorg/tenetur-eius/dedupe-by]: https://github.com/kollorg/tenetur-eius/tree/main/dedupe-by

[@kollorg/tenetur-eius/dedupe]: https://github.com/kollorg/tenetur-eius/tree/main/dedupe

[@kollorg/tenetur-eius/empty]: https://github.com/kollorg/tenetur-eius/tree/main/empty

[@kollorg/tenetur-eius/every-by]: https://github.com/kollorg/tenetur-eius/tree/main/every-by

[@kollorg/tenetur-eius/every]: https://github.com/kollorg/tenetur-eius/tree/main/every

[@kollorg/tenetur-eius/fill]: https://github.com/kollorg/tenetur-eius/tree/main/fill

[@kollorg/tenetur-eius/filter-map]: https://github.com/kollorg/tenetur-eius/tree/main/filter-map

[@kollorg/tenetur-eius/filter]: https://github.com/kollorg/tenetur-eius/tree/main/filter

[@kollorg/tenetur-eius/first]: https://github.com/kollorg/tenetur-eius/tree/main/first

[@kollorg/tenetur-eius/flow]: https://github.com/kollorg/tenetur-eius/tree/main/flow

[@kollorg/tenetur-eius/for-each]: https://github.com/kollorg/tenetur-eius/tree/main/for-each

[@kollorg/tenetur-eius/head]: https://github.com/kollorg/tenetur-eius/tree/main/head

[@kollorg/tenetur-eius/incrspace]: https://github.com/kollorg/tenetur-eius/tree/main/incrspace

[@kollorg/tenetur-eius/intersection-by-hash]: https://github.com/kollorg/tenetur-eius/tree/main/intersection-by-hash

[@kollorg/tenetur-eius/intersection]: https://github.com/kollorg/tenetur-eius/tree/main/intersection

[@kollorg/tenetur-eius/last]: https://github.com/kollorg/tenetur-eius/tree/main/last

[@kollorg/tenetur-eius/length]: https://github.com/kollorg/tenetur-eius/tree/main/length

[@kollorg/tenetur-eius/linspace]: https://github.com/kollorg/tenetur-eius/tree/main/linspace

[@kollorg/tenetur-eius/logspace]: https://github.com/kollorg/tenetur-eius/tree/main/logspace

[@kollorg/tenetur-eius/map]: https://github.com/kollorg/tenetur-eius/tree/main/map

[@kollorg/tenetur-eius/mapn]: https://github.com/kollorg/tenetur-eius/tree/main/mapn

[@kollorg/tenetur-eius/none-by]: https://github.com/kollorg/tenetur-eius/tree/main/none-by

[@kollorg/tenetur-eius/none]: https://github.com/kollorg/tenetur-eius/tree/main/none

[@kollorg/tenetur-eius/nth]: https://github.com/kollorg/tenetur-eius/tree/main/nth

[@kollorg/tenetur-eius/pipeline-thunk]: https://github.com/kollorg/tenetur-eius/tree/main/pipeline-thunk

[@kollorg/tenetur-eius/pipeline]: https://github.com/kollorg/tenetur-eius/tree/main/pipeline

[@kollorg/tenetur-eius/pop]: https://github.com/kollorg/tenetur-eius/tree/main/pop

[@kollorg/tenetur-eius/push]: https://github.com/kollorg/tenetur-eius/tree/main/push

[@kollorg/tenetur-eius/reject]: https://github.com/kollorg/tenetur-eius/tree/main/reject

[@kollorg/tenetur-eius/replicate-by]: https://github.com/kollorg/tenetur-eius/tree/main/replicate-by

[@kollorg/tenetur-eius/replicate]: https://github.com/kollorg/tenetur-eius/tree/main/replicate

[@kollorg/tenetur-eius/shift]: https://github.com/kollorg/tenetur-eius/tree/main/shift

[@kollorg/tenetur-eius/slice]: https://github.com/kollorg/tenetur-eius/tree/main/slice

[@kollorg/tenetur-eius/some-by]: https://github.com/kollorg/tenetur-eius/tree/main/some-by

[@kollorg/tenetur-eius/some]: https://github.com/kollorg/tenetur-eius/tree/main/some

[@kollorg/tenetur-eius/step]: https://github.com/kollorg/tenetur-eius/tree/main/step

[@kollorg/tenetur-eius/strided-by]: https://github.com/kollorg/tenetur-eius/tree/main/strided-by

[@kollorg/tenetur-eius/strided]: https://github.com/kollorg/tenetur-eius/tree/main/strided

[@kollorg/tenetur-eius/to-array-view-right]: https://github.com/kollorg/tenetur-eius/tree/main/to-array-view-right

[@kollorg/tenetur-eius/to-array-view]: https://github.com/kollorg/tenetur-eius/tree/main/to-array-view

[@kollorg/tenetur-eius/union]: https://github.com/kollorg/tenetur-eius/tree/main/union

[@kollorg/tenetur-eius/unique-by-hash]: https://github.com/kollorg/tenetur-eius/tree/main/unique-by-hash

[@kollorg/tenetur-eius/unique-by]: https://github.com/kollorg/tenetur-eius/tree/main/unique-by

[@kollorg/tenetur-eius/unique]: https://github.com/kollorg/tenetur-eius/tree/main/unique

[@kollorg/tenetur-eius/unitspace]: https://github.com/kollorg/tenetur-eius/tree/main/unitspace

[@kollorg/tenetur-eius/unshift]: https://github.com/kollorg/tenetur-eius/tree/main/unshift

[@kollorg/tenetur-eius/while-each]: https://github.com/kollorg/tenetur-eius/tree/main/while-each

<!-- </toc-links> -->

</section>

<!-- /.links -->
