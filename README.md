# polymer-funky-flux
A [flux-comparison](https://github.com/voronianski/flux-comparison) demo using Polymer and Reflux via [funk](https://github.com/devinivy/funk)

## Give it a whirl!

Check it out on the web [here](http://devinivy.github.io/polymer-funky-flux/) or install locally and hack away!
```sh
git clone git@github.com:devinivy/polymer-funky-flux.git
cd polymer-funky-flux
bower install
python -m SimpleHTTPServer # or equivalent

# Now navigate to http://localhost:8000
```

## Polymer with flux?
Polymer is a framework for creating web components.  It lets you hurl data around your app willy-nilly because Polymer's concern is not with building stateful applications.  But we do want to build entire apps using Polymer!  So we need to decide on a sane method of housing and manipulating our application's state– Polymer does not solve this issue on its own.

Flux is where the sanity begins.  "Flux" simply refers to a _pattern_ for managing state within your application.  It was pioneered by Facebook and is used broadly in the React ecosystem.  There are several libraries that implement all the fluxy machinery necessary for use in a web application.  Usually these libraries are small, partially because flux is simple.

The [**funk**](https://github.com/devinivy/funk) project marries Polymer with a particular implementation of flux named Reflux.  Reflux is a good fit for use with Polymer because,

  1. It's written in terms of mixins that work out-of-the-box as Polymer behaviors.
  2. Reflux's store components are created similarly to the `Polymer({/* definition */})` syntax for creating web components, their definitions also consisting of methods and properties.

Together this means Reflux both feels familiar to Polymer developers and also integrates into a Polymer app with minimal friction.  Funk makes the transition seamless by additionally gluing together Reflux's stores and Polymer's data-binding.

Reflux and Polymer look pretty darn good together!

## Testing
Evaluating how actions are interpreted by stores is one good way to test your application.  Check out the `test` folder to see how to test an app built on Polymer and Reflux.  The tests can be run right before your eyes by navigating [here](http://devinivy.github.io/polymer-funky-flux/test).

## More info
 - [Funk](https://github.com/devinivy/funk) ties Reflux and Polymer together
 - The [Refluxjs readme](https://github.com/reflux/refluxjs/blob/master/README.md) provides good documentation and examples of using Reflux
 - The defacto [flux overview](https://facebook.github.io/flux/docs/overview.html) by Facebook explains the core mechanics of flux– note that they refer to their own implementation of flux (which is not Reflux)
 - Facebook [explains](https://youtu.be/nYkdrAPrdcw?t=7m17s) why they dropped MVC for flux
