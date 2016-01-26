# polymer-funky-flux
A [flux-comparison](https://github.com/voronianski/flux-comparison) demo using Polymer and Reflux via [funk](https://github.com/devinivy/funk)

## Give it a whirl!
```sh
git clone git@github.com:devinivy/polymer-funky-flux.git
cd polymer-funky-flux
bower install
python -m SimpleHTTPServer
# Now navigate to http://localhost:8000
```

## Polymer with flux?
Polymer is a framework for creating web components.  It let's you sling data around your app all willy-nilly because Polymer's concern is not with building stateful applications.  But we do want to build entire apps using Polymer!  So we need to decide on a sane method of housing and manipulating application state.

Flux is where the sanity begins.  "Flux" simply refers to a _pattern_ for managing state within your application.  It was pioneered by Facebook and is used broadly in the React ecosystem.  There are several libraries that implement all the fluxy machinery necessary for use in a web application.  Usually these libraries are small, partially because flux is simple.

The [**funk**](https://github.com/devinivy/funk) library marries Polymer and one implementation of flux named Reflux.  Reflux is a good fit for use with Polymer because,

  1. It's written in terms of mixins that work out-of-the-box as Polymer behaviors.
  2. Reflux's store components are created similarly to the `Polymer({/* definition */})` syntax.

Together this means Reflux both feels familiar to Polymer developers and also integrates into a Polymer app with minimal friction.  Funk makes the transition seamless by additionally gluing together Reflux's stores and Polymer's data-binding.

Reflux and Polymer look pretty darn good together!
