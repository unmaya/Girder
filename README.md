[Girder Site Files](http://comfypixel.com/Girder/)
====================

A simple CSS grid toolkit built on Sass. This is the demo source for the github page, it includes a basic starter kit with some responsive examples and grid uses.

---

# About the demo
This page is built with Girder to test functionality and for general reference.

**Example HTML**
```HTML
<main class="content row">
	<article> My main column covers two thirds of the page. </article>
	<aside> This sidebar content occupies one third of the page. </aside>
</main>
```
The Sass for this example could look like this:
```SCSS
// Define unit spacing in pixels or turn it to ems automagically
$gutters: emCalc(20px);
// Include girder (modules next to this partial)
@import girder;

// You can have a fixed width / centered container or make it fluid
$container-width: 1322px;

main.content {
	article { @include(two-thirds); }
	aside {
		@include(one-third);
		background: #ddd;
	}
}
```
# Installation / Requirements
1. Once you've installed the Sass Gem you can get the latest version of Girder from this repo directly or with Bower: ```bower install girder --save``` You can also [download all the example files](http://comfypixel.com/Girder/Girder_example_files_v04.zip)

a.	**girder.scss**
b.	**/girder_modules/**

Include the scss files before your base styles:
```SCSS
@import girder;

// Follow with your base styles
```

2. Start building your markup and hook up the grid simply by adding rows and including the mixins in your selectors like this:

```SCSS
// Units go as small as one-sixth of any container, mix and match as needed
@include unit(three-fourths); // Match fourths
@include unit(one-third); // Match thirds
footer { @include clearfix; } // Clear anything without a class
```
[Check the example](http://comfypixel.com/Girder/), inspect, poke and download the source to see exactly how it works.

## Optional
Girder is made with responsive design in mind and can easily adapt to a mobile-first approach using the Breakpoint plugin for Compass. Just make sure you [install the gem](http://rubygems.org/gems/breakpoint) and include the module by un-commenting these lines in the settings:

````SCSS
@import "breakpoint";
@import "girder_modules/girder_responsive";
````

### This project is open to suggestions, forks, experiments, etc
