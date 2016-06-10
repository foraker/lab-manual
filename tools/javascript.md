# JavaScript

JavaScript provides dynamic experiences in the browser for our users. At the time of writing, we prefer to write our JavaScript in CoffeeScript, because of it's implementation of classical inheritance, clean syntax, and other niceties.

## Web

- The [CoffeeScript][cs] site provides a comprehensive overview of the language.
- Please write CoffeeScript according to the [CoffeeScript Style Guide][cssg]. Just like the Ruby Style Guide, if you use a style we don't agree with, we'll let you know during the pull request process.
- Many of our applications make use of the [Backbone.js][bb] library to implement MVC on the client side.
- Many of our applications also use the [Underscore.js][us] utility library, which is itself a dependency of Backbone.js.
- [Traction][t] is a Foraker Labs authored library of extensions to Backbone.js, used in a few of our projects.
- Though we don't currently have any projects in production using it, we are excited about the convention over configuration embodied in [Ember][e], and are enthusiastically following its progress.

## Books

- [Speaking JavaScript][sj]

[cs]: http://coffeescript.org
[cssg]: https://github.com/polarmobile/coffeescript-style-guide
[bb]: http://backbonejs.org
[us]: http://underscorejs.org
[t]: https://github.com/foraker/traction
[sj]: http://speakingjs.com/es5
[e]: http://emberjs.com
