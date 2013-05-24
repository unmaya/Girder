Girder 0.2.0 (Alpha)
====================

A simple grid toolkit built on Sass. Its responsive, semantic, silent and minimal but its also going to include some utility CSS to build prototypes quickly. Mostly for my little projects and general amusement.

**Note: Its experimental code & constantly changing. The CSS output still contains debug information**

# Why build another css grid?
Because I can :) No, really. I couldn't find exactly what I was looking for so I decided to spin my own solution over a rainy weekend. Its influenced by bits of code from various sources; the main difference is I'm scaling way down from the other frameworks I've found. I just want a small, responsive and semantic grid to build on Sass. I'm drawing inspiration from a bunch of sources so I started fresh instead of forking an existing project. -I'm looking to keep it super simple though.

---

# How it works (currently)
1. Install the Compass Gem which includes Sass. ```gem install compass```
2. Once you have your project environment, copy the Sass folder from this Repo. You only need two things: **girder.scss** and **/girder_modules/** - everything else is optional.
3. Start building your markup and hook into the grid simply by including the mixins in your selectors like this: ```@include unit(two-thirds);``` and wrapping rows with the ```.row``` class.

Thats it for now. I'll include some reference info for using the grid as it develops.

_Some functionality is not available yet... its a work in progres :)_

Girder will be built to take advantage of Sass but I'm also making a plain css version of the grid for other use cases. The css version however, will rely on presentational classes to structure the markup (which is exactly what I'm looking to avoid here).
