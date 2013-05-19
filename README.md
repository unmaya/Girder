Girder 0.1.0 (Alpha)
====================

A simple grid toolkit built on Sass. It will be responsive, semantic, silent and minimal but it will also include some utility css to develop fast prototypes. Mostly, for my little projects and general amusement.

**Its Still Experimental Code And Changing Often**

# Why build another css grid?
Because I can :) No, really. I couldn't find exactly what I was looking for so I decided to spin my own solution over a rainy weekend. Its influenced by bits of code from various sources; the main difference is I'm scaling way down from the other frameworks I've found. I just want a small, responsive and semantic grid to build on Sass. I'm drawing inspiration from a bunch of sources so I started fresh instead of forking an existing project. -I'm looking to keep it super simple though.

---

# How it works (currently)
1. Install the Compass Gem which includes Sass. ```gem install compass```
2. Once you have your project environment copy the Sass folder from this Repo
3. Start building your markup and hook into the grid simply by including the mixins in your selectors like this: ```@include unit(two-thirds);``` '

Thats it for now. I'll include some reference info for grid usage as it develops.

_Note:_ Some functionality is not available yet (its a work in progress).

Girder will be built to take advantage of Sass but I'm also making a plain css version of the grid for other use cases. The css version however, will rely on presentational classes to structure the markup (which is exactly what I'm looking to avoid here).
