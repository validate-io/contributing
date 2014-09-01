Contributing
============

[Validate.io](https://github.com/validate-io/overview) is a collection of validation utilities. To contribute to [Validate.io](https://github.com/validate-io/overview), please follow the guide provided below.


## JavaScript

[Validate.io](https://github.com/validate-io/overview) uses the following JavaScript [style guide](https://github.com/kgryte/javascript-style-guide). Most importantly, modules should be written in the same style and idiom.


## Generator

You are encouraged to use the [Yeoman](http://yeoman.io) Validate.io [generator](https://github.com/validate-io/generator-validate-io). The generator creates a base scaffold from which to build your validation module.

Before using the generator, you should create a remote repository on [Github](https://github.com/validate-io). The generator will use the module and repository names to generate the remote URLs included in the `package.json`. Additionally, the generator takes care of setting the remote origin for the local Git repository, so you can begin pushing code immediately after generation.


## Modules

In most cases, the main file for each module should export a function which performs validation.


### Type Checking

Where necessary, you are __strongly encouraged__ to type check input arguments. While including checks leads to longer modules and more required tests, doing so helps define user expectations and allows users to more easily debug their code.

``` javascript
// Do:
function isURL( url ) {
	if ( typeof url !== 'string' ) {
		return false;
	}
	// Check for URL...
}

// Don't:
function isURL( url ) {
	// Check for URL...
}
```


## Tests

All modules should instrument testing. Currently, [Mocha](http://visionmedia.github.io/mocha) is the preferred test framework with [Chai](http://chaijs.com) assertions. For code coverage, you are encouraged to use [Istanbul](https://github.com/gotwarlost/istanbul).

If you use the Validate.io [generator](https://github.com/validate-io/generator-validate-io), the above test modules are included. Strive for 100% code coverage.


---
## License

[MIT license](http://opensource.org/licenses/MIT). 


---
## Copyright

Copyright &copy; 2014. Athan Reines.