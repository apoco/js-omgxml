# js-omgxml
Feature-complete XML implementation? OMG!

## Project Manifesto

Sometimes, you just have to read or write XML. As a Node developer, every single time I need to do anything
with XML, I only find XML libraries that are:

* Incomplete implementations; yes I really _do_ need XML namespaces and CDATA.
* Bindings to native libraries that either don't build on all platforms or segfault
* Leaky-abstraction Wrappers
* Riddled with three-year-old bugs

This may be hubris, but I want to create an XML library that:

* Passes all conformance tests; why even release and XML library before then?
* Supports all the functionality you usually need when working with XML; you shouldn't need a whole
  suite of tools lacking design fidelity. To me, this means:
    * A streaming XML parser (that can also take strings)
    * A streaming XML writer (that can also create strings)
    * A DOM
    * XPath
* Is pure JS; JavaScript is totally powerful enough to implement XML; why bring C into this?
* Ignores the needs of ancient JS implementations; ain't nobody got time for that, and browsers have their
  own DOM implementation anyway.

Once these core goals are completed, then it's a foundation you can reliably wrap with conveniences without
compromising on XML compliance. By conveniences, I mean:

1. A fluent API wrapper around the DOM
2. Error correction for less-strict parsing
3. Maybe a native XSLT engine?

## Project Status

Here are the project tasks in priority order (subject to change):

Prior to 1.0 release:

* Streaming XML parser
* Streaming XML serializer
* DOM level 1
* DOM level 2
* DOM level 3
* XPath 1.0
* XPath 2.0

Future plans:

* Fluent API
* XSLT
