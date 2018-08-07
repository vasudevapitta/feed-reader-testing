# Feed Reader Testing
This project consists of test suites built using the Jasmine framework to test against a RSS Feed app.

## Running the application

You may get the files by either fork the repository from this page or download the files, unzip and extract
the files to where you want them in your directory.
Once the files are locally stored in your computer open the index.html.

If you would like to run gulp inorder to concat and minify the CSS, JS files and optimize any images you may
first place all your source files in a directory called src.

Then do npm init to create a package.json file with the meta data and the dependencies listed in it.

Then install gulp either globally by
npm install -g gulp

or locally as a dev dependency by
npm install gulp --save-dev

Then create a file by the name gulpfile.js and write all your gulp tasks in it to perform tasks like
concatenating, minifying, optimizing images, converting sass files to css (if you have any sass files)
pipe them one after the other.

Pipe the final files into a folder called dist.
check out more about [Gulp here](https://www.npmjs.com/package/gulp-install)

You may install browser-sync as a dependency and add a watch task for expressive live editing (To see changes you make instantly in 
the browser without having to refresh the browser). You may also set up expressive live editing using a text editor like Brackets
which provides instant preview of the changes you make. Alternatively you may code in using a chrome extension for live editing.
Check out more about [Browser-sync](https://browsersync.io/docs)

You can write a gulp.watch task on the files to let gulp watch for any changes from the src folder
can serve the files using a local file sever while using browserify.

## Using the application
Test results will appear at the bottom of the page.
RSS feeds can be changed by clicking the menu icon at the top left of the page.
Clicking on any entry of a feed will take you to that article.

## Inspecting the feedReader.js file
Each suite starts with a describe (with a name) and it contains a "it" spec/block which has a set of expectations
The expectation has an actual and a matcher and a value for the matcher.
All the expectations within an "it" block must evaluate to true in order to pass the test suite.
Each file can contain several suites.
You may find more information about [Jasmine frame work](https://jasmine.github.io/)

## Most commonly used Jasmine Matchers
expect(instance).toBe(instance);
expect(number).toBeCloseTo(number, decimalPlaces);
expect(mixed).toBeDefined();
expect(mixed).toBeFalsy();
expect(number).toBeGreaterThan(number);
expect(number).toBeLessThan(number);
expect(number).toBeNaN();
expect(mixed).toBeNull();
expect(mixed).toBeTruthy();
expect(mixed).toBeUndefined();
expect(array).toContain(member);
expect(mixed).toEqual(mixed);
expect(spy).toHaveBeenCalled();
expect(spy).toHaveBeenCalledTimes(number);
expect(spy).toHaveBeenCalledWith(...arguments);
expect(mixed).toMatch(pattern);
expect(fn).toThrow(string);
expect(fn).toThrowError(string);
