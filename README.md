Girder 0.3.0 (Alpha) [demo](http://unmaya.github.io/Girder/)
====================

A simple CSS grid toolkit built on Sass. Its flexible, semantic, responsive and minimalistic. It includes some utilities to build prototypes quickly so I use it for smaller projects and as a kickstarter template.
**Why build another css grid?** Because I can :) No, really. I couldn't find exactly what I was looking for so I decided to spin my own solution over a rainy weekend. I'm drawing inspiration from all over but I'm looking to keep things super simple.

---

# How it works
Girder is a simple yet versatile grid designed for use in small to medium projects. Its best suited for building with Sass, a fantastic pre-processor but you can also use plain CSS.

**Example?**
You can write your html with semantic classes to target elements in CSS or use the cascade to add structure:
```HTML
<main class="content row">
	<article> My main column covers two thirds of the page. </article>
	<aside> This sidebar content occupies one third of the page. </aside>
</main>
```
The Sass for this example could look like this:
``` SCSS
// Pass gutter width in pixels or turn it to ems automagically
$gutters: emCalc(20px);

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
1. Install the Compass Gem which includes Sass: ```sudo gem install compass```
2. Copy the Sass folder from this Repo. You only need two things (everything else is optional):

	**girder.scss**

	**/girder_modules/**

3. Start building your markup and hook up the grid simply by adding rows and including the mixins in your selectors like this:
```scss @include unit(three-fourths); ```
```scss @include unit(one-third); ```
```scss @include unit(two-fifths); ```

4. **Optional** Girder is made to be responsive and can easily adapt to a mobile-first approach using the Breakpoint plugin for Compass. Just make sure you include the module by uncommenting this line in the Girder settings file:
```@import "girder_modules/girder_responsive";```

Wrap multi-column rows with the ```.row``` class. Nest rows and mix grid units to achieve your desired results. You can remove gutters, push units and use sophisticated breakpoint plugins to make Girder fully responsive. [Check the example](http://comfypixel.com/Girder/), inspect, poke and download all the files to see exactly how it works.

Girder is built to take advantage of Sass but I'm also making a plain CSS version of the grid for other uses. The CSS version however, will rely on presentational classes to structure the markup (which is exactly what I'm looking to avoid here).
