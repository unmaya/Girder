Girder 0.4.0 (Beta) [demo](http://comfypixel.com/Girder/)
====================

A simple CSS grid toolkit built on Sass. Its flexible, semantic, responsive and minimalistic. It includes some utilities to build prototypes quickly so I use it for smaller projects and as a kickstarter template.
**Why build another css grid?** Because I can :) No, really. I couldn't find exactly what I was looking for so I decided to spin my own solution over a rainy weekend. I'm drawing inspiration from all over but I'm looking to keep things super simple.

---

# How it works
Girder is a simple yet versatile grid designed for small to medium projects. Its best suited for building with Sass, a fantastic pre-processor but you can also use plain CSS. Build flexible layouts divided into logical sections. It uses silent classes (placeholders) to structure content in HTML and keeps your Markup free of excess presentational classes like "unit_1of4", "small-2", "grid4".

**Example?**
You can write HTML with custom classes to target elements or use the cascade with base selectors:
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
Copy the Sass folder from this Repo. or [Download all the example files](http://comfypixel.com/Girder/girder_package_v04.zip). You only need two things, the main settings file and the modules folder (everything else is optional):

*	**girder.scss**
*	**/girder_modules/**

Include the scss files before your base styles:
```SCSS
@import girder;

// Follow with your base styles
```

1. Unless you're using the plain CSS version be sure the Compass Gem is installed which includes Sass, if you're not sure issue this command in the console: ```sudo gem install compass```
2. Start building your markup and hook up the grid simply by adding rows and including the mixins in your selectors like this:

```SCSS
// Units go as small as one-sixth of any container, mix and match as needed
@include unit(three-fourths); // Match fourths
@include unit(one-third); // Match thirds
footer { @include clearfix; } // Clear anything without a class
```

**To use plain CSS** you just add the classes to the markup like this:
```HTML
<!-- Be sure to include the girder.css file in your document -->
<main class="content row">
	<article class="unit two-thirds"> My main column covers two thirds of the page. </article>
	<aside class="unit one-third"> This sidebar content occupies one third of the page. </aside>
	<footer class="clear">Awesome footer</footer>
</main>
```

**Some familiar options:** Wrap multi-column rows with the ```.row``` class. Nest rows and mix grid units to achieve your desired results. You can remove gutters, push units, add media queries or use any number of plugins for Sass. [Check the example](http://comfypixel.com/Girder/), inspect, poke and download the source to see exactly how it works.

## Optional
Girder is made with responsive design in mind and can easily adapt to a mobile-first approach using the Breakpoint plugin for Compass. Just make sure you [install the gem](http://rubygems.org/gems/breakpoint) and include the module by un-commenting these lines in the settings:

````SCSS
@import "breakpoint";
@import "girder_modules/girder_responsive";
````

### This project is open to suggestions, forks, experiments, etc
