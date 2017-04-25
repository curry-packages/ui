ui: Declarative User Interfaces
===============================

This directory contains the libraries to implement user interfaces
as described in the paper

M. Hanus, C. Kluss:
[Declarative Programming of User Interfaces](http://dx.doi.org/10.1007/978-3-540-92995-6_2)
Proc. of the 11th International Symposium on Practical Aspects of
Declarative Languages (PADL'09), Springer LNCS 5418, pp. 16-30, 2009

--------------------------------------------------------------------------

The following changes might be necessary for a local installation:

* Redefine in UI2HTML.curry the path "includeURL" to a URL where the
  auxiliary files of this directory are stored.
  For instance, if you define in UI2HTML.curry

      includeURL = "http://MYURL/ui/"

  then the directory with URL http://MYURL/ui/ should contain
  the (public accessible!) files

      Action.js
      Throbber.gif
      Throbber.png
      ajaxrequest.js
      default.css
      prototype.js

* Redefine in ajaxrequest.js the URL for "Throbber" images, e.g., define

      var busyImage  = "http://MYURL/ui/Throbber.gif";
      var readyImage = "http://MYURL/ui/Throbber.png";

  before you put this file to the location http://MYURL/ui/ajaxrequest.js

--------------------------------------------------------------------------

Explanation of some files in the `src` directory:


UI.curry: Interface for ui descriptions

UI2GUI.curry : UIs as GUI applications
UI2HTML.curry: UIs as web applications

ajaxrequest.js: used by UI2HTML for Ajax requests and DOM manipulations

GUI2HTML.curry: GUIs as web applications

TypedUI2GUI.curry: typed UIs as GUI applications
TypedUI2HTML.curry: typed UIs as web applications

GUI.curry: slightly altered GUI library
HTML.curry: HTML library with extensions for Ajax 

SpicyWeb.curry: slightly altered SpicyWeb library
Json.curry - JSON library


The directory `examples` contains some examples for the use
of these libraries.

--------------------------------------------------------------------------
