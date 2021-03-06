# cljs-devtools

**DANGER ZONE - WORK IN PROGRESS - EXPERIMENTAL APIs**

[![Build Status](https://travis-ci.org/binaryage/cljs-devtools.svg)](https://travis-ci.org/binaryage/cljs-devtools)

Better presentation of ClojureScript values in Chrome Devtools:

<img src="https://dl.dropboxusercontent.com/u/559047/cljs-formatter-prototype.png">

## Integration in your own project

Add devtools dependency into your Leiningen's project.clj:

[![Clojars Project](http://clojars.org/binaryage/devtools/latest-version.svg)](http://clojars.org/binaryage/devtools)

To activate it. At some point you have to call `install!` from `devtools.core` namespace. Ideally run this at launch time of your app.

    (ns your-project.core
      (:require [devtools.core :as devtools]))
    
    (devtools/install!)
    
    (.log js/console (range 200))

## See [sample project](https://github.com/binaryage/cljs-devtools-sample)

## Enable Custom formatters in your Chrome (Canary)

For now you must use Chrome Canary (worked in 48.0.2537.0 canary (64-bit) under Mac).

##### Turn on custom formatters:

  * Open DevTools.
  * Go to Settings: (Click "three dots" menu in upper right corner of DevTools > Menu > Settings F1)
  * Check "Enable custom formatters".
  * Close Dev Tools.
  * Open Dev Tools.

#### License [MIT](https://raw.githubusercontent.com/binaryage/cljs-devtools/master/LICENSE.txt)