Girder (Alpha)
=============

A simple grid toolkit built on Sass. It will be responsive, semantic, silent and minimal but it will also include some utility css to develop fast prototypes. Mostly, for my little projects and general amusement.

**Its Not Working Yet!**

# Why build another css grid?
Because I can :) No, really. I couldn't find exactly what I was looking for so I decided to spin my own during a rainy weekend. Its heavily influenced by bits from Eric Mayer, Zurb, Team-sass, Cobyism and other awesome coders. The difference is I'm scaling down from the other frameworks / systems I've found. I'm also mixing a bunch of sources so I started fresh instead of forking an existing project. I'll include some of the great techniques I've found in the wild -I'm looking to keep it super simple though.

_I'll add more details soon..._

---

# How it works (currently)
Install the Compass Gem which includes Sass. You'll be able to start building your markup and hook into the grid simply by including the mixins in your selectors like this: ```@include unit-two-thirds;``` Thats it for now. _Note:_ Some grid functionality is not available yet! (its a work in progress)

Girder will be built to take advantage of Sass but I'm also making a plain css version of the grid. The css version however, will rely on presentational classes to structure the markup (exactly what I'm looking to avoid here).
