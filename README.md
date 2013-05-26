Girder 0.2.0 (Alpha) [demo](http://unmaya.github.io/Girder/)
====================

A simple grid toolkit built on Sass. Its responsive, semantic, and a minimalist solution. Its also going to include some utility CSS to build prototypes quickly. Mostly for my small projects and general amusement.

---

# How it works
Girder is a simple yet versatile grid designed for use in small to medium projects. Its best suited for building with Sass, a fantastic pre-processor but you can also use plain CSS.

** Example? **
You could write your html with semantic classes to target elements in CSS or use the cascade to add structure:
```HTML
<main class="content">
	<article> My main column covers two thirds of the page. </article>
	<aside> This sidebar content occupies one third of the page. </aside>
</main>
```
The Sass for this example could look like this:
``` SASS
// Pass gutter width in pixels or turn it to ems automagically
$gutters: emCalc(20px);

// You can have a fixed width / centered container
$container-width: auto;

main.content {
	article { @include(two-thirds); }
	aside { @include(one-third); }
}
```

# Installation / Requirements
1. Install the Compass Gem which includes Sass: ```sudo gem install compass```
2. Copy the Sass folder from this Repo. You only need two things (everything else is optional):

	**girder.scss**

	**/girder_modules/**

3. Start building your markup and hook up the grid simply by including the mixins in your selectors like this:

```scss
.content {
	@include unit(two-thirds);
}
.sidebar {
	@include unit(one-third);
}
```

Wrap multi-column rows with the ```.row``` class. Optionally if you are using the responsive module you'll need the breakpoint gem: ```sudo gem install breakpoint```

Girder is built to take advantage of Sass but I'm also making a plain CSS version of the grid for other uses. The CSS version however, will rely on presentational classes to structure the markup (which is exactly what I'm looking to avoid here).
