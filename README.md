# cloudkit-js-demo

_A look at CloudKit JS_

## Motivation

I use the iOS Notes app to scribble thoughts and lists and the iOS Reminders app for ToDos. Can the CloudKit Notes/Reminders backend-as-a-service power custom web applications or integrate with other web services?

**Update:** CloudKit JS doesn’t appear to offer a way to access Notes or Reminders via an API.

## Links

* [CloudKit JS homepage](https://developer.apple.com/documentation/cloudkitjs)
* [CloudKit Quick Start](https://developer.apple.com/library/archive/documentation/DataManagement/Conceptual/CloudKitQuickStart/Introduction/Introduction.html#//apple_ref/doc/uid/TP40014987)

## Initial Thoughts

* Under the “Before You Begin” section:

    > [C]reate an iOS or Mac app that uses CloudKit to store your app’s data.

    — https://developer.apple.com/documentation/cloudkitjs

    So a development must create a iOS or macOS app before using CloudKit JS?
* [“cloudkit” on npmjs.com](https://www.npmjs.com/package/cloudkit) doesn’t appear to be an official package. Searching for “cloudkit” on npmjs.com [doesn’t yield many results](https://www.npmjs.com/search?q=cloudkit).
* There's no open CloudKit JS code on the [github.com/apple org](https://github.com/apple).
* The CloudKit JS library appears to be browser-only, and only available via Apple’s hosted script:

    > Embed CloudKit JS in your webpage using the `script` tag and link to Apple’s hosted version of CloudKit JS at `https://cdn.apple-cloudkit.com/ck/2/cloudkit.js`.
    >
    > ```
    > <script src="https://cdn.apple-cloudkit.com/ck/2/cloudkit.js">
    > ```

    — https://developer.apple.com/documentation/cloudkitjs
* [tsl-apple-cloudkit exists on typescriptlibs.org](https://typescriptlibs.org/tsl-apple-cloudkit/), but the source is untrustworthy.
* [Questions for “cloudkit” and “javascript” on stackoverflow.com](https://stackoverflow.com/questions/tagged/cloudkit+javascript) don’t yield many results (similar for [“cloudkit-js”](https://stackoverflow.com/search?q=cloudkit-js) and [“cloudkit-web-services”](https://stackoverflow.com/questions/tagged/cloudkit-web-services))
* CloudKit sounds like a service over [CouchDB](http://couchdb.apache.org):

    > An app has access to both a public and private database in each container. The _public database_ is for storing user and app data that is shared between all instances of the app…There’s a _private database_ for each user of your app, but the app only has access to the private database of the current user.

    — [“Enabling CloudKit in Your App” on developer.apple.com](https://developer.apple.com/library/archive/documentation/DataManagement/Conceptual/CloudKitQuickStart/EnablingiCloudandConfiguringCloudKit/EnablingiCloudandConfiguringCloudKit.html#//apple_ref/doc/uid/TP40014987-CH2-SW1)

* Many of the [developer.apple.com](https://developer.apple.com/documentation/) pages for CloudKit JS have a “this page no longer updated” message at the top.
* The [“CloudKit Catalog: An Introduction to CloudKit (Cocoa and JavaScript)”](https://developer.apple.com/library/archive/samplecode/CloudAtlas/Introduction/Intro.html#//apple_ref/doc/uid/TP40014599) is very outdated (“Version 6.0, 2016-09-13”) and contains an example with Node.js antipatterns and aged front-end web practices.
* The [CloudKit JS API documentation](https://developer.apple.com/documentation/cloudkitjs/cloudkit) is a little weird:
    * The sections include “Classes,” “Constants,” “Enumerations,” “Structures,” and [pages refer to types as “dictionary”](https://developer.apple.com/documentation/cloudkitjs/cloudkit/record)…this sounds like a native library!
    * Method documentation pages [don’t include links to return types](https://developer.apple.com/documentation/cloudkitjs/cloudkit/1628647-getdefaultcontainer); in some cases [the return type isn’t named](https://developer.apple.com/documentation/cloudkitjs/cloudkit/container/1773251-getdatabasewithdatabasescope).
    * [`Promise`](https://developer.apple.com/documentation/cloudkitjs/cloudkit/1628514-promise) is a property? Modern browsers and Node.js have this as a native object.
    * Some classes appear to [expose a property to identify their type](https://developer.apple.com/documentation/cloudkitjs/cloudkit/useridentitiesresponse#topics), which is a little un-JavaScript-y (prefer `instanceof` or clearer data structures).
* CloudKit doesn’t seem to provide an API to Notes nor Reminders: a [stackoverflow.com answer](https://stackoverflow.com/a/53289466) indicates that accessing via the web for a server is impossible.


