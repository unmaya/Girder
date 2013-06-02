Girder  v.0.3.0 (Alpha)
=======================

A simple grid toolkit built on Sass. Its flexible, semantic, responsive and minimalistic. Its designed for quick prototyping and I use it in small projects and for general amusement.

**Why build another css grid?** Because I can :) No, really. I couldn't find exactly what I was looking for so I decided to spin my own solution over a rainy weekend. Its influenced by bits of code from various sources but scaled way down from what I've found. I just want a small, responsive and semantic grid to build with (on Sass). I'm drawing inspiration from a bunch of sources so I started fresh instead of forking an existing project. -I'm looking to keep it super simple though.

---

# How it works
1. Install the Compass Gem which includes Sass: ```sudo gem install compass```
2. Copy the Sass folder from this Repo. You only need two things (everything else is optional):

	**girder.scss**
	**/girder_modules/**

3. Include girder.scss in your project with ```@import girder;```

# Usage guide
Start building your markup and hook it up to the grid simply by including the mixins in your selectors like this:

```scss
.content {
	@include unit(two-thirds);
}
.sidebar {
	@include unit(one-third);
}
```

Wrap multi-column rows with the ```.row``` class. Optionally if you are using the responsive module you'll need the breakpoint gem: ```sudo gem install breakpoint```

Thats it for now. _This is a work in progres :)_

Girder is built to take advantage of Sass but I'm also making a plain CSS version of the grid for other uses. The CSS version however, will rely on presentational classes to structure the markup (which is exactly what I'm looking to avoid here).
