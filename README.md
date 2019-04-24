# cloudkit-js-demo

_A look at CloudKit JS_

## Motivation

I use the iOS Notes app to scribble thoughts and lists and the iOS Reminders app for ToDos. Can the CloudKit Notes/Reminders backend-as-a-service power custom web applications or integrate with other web services?

## Links

* [CloudKit JS homepage](https://developer.apple.com/documentation/cloudkitjs)
* [CloudKit Quick Start](https://developer.apple.com/library/archive/documentation/DataManagement/Conceptual/CloudKitQuickStart/Introduction/Introduction.html#//apple_ref/doc/uid/TP40014987)

## Initial Thoughts

* [_cloudkit_ on npmjs.com](https://www.npmjs.com/package/cloudkit) doesn't appear to be an official package. Searching for "cloudkit" on npmjs.com [doesn't yield many results](https://www.npmjs.com/search?q=cloudkit).
* There's no open CloudKit JS code on the [github.com/apple org](https://github.com/apple).
* The CloudKit JS library appears to be browser-only, and only available via Apple's hosted script:

    > Embed CloudKit JS in your webpage using the `script` tag and link to Apple’s hosted version of CloudKit JS at `https://cdn.apple-cloudkit.com/ck/2/cloudkit.js`.
    >
    > ```
    > <script src="https://cdn.apple-cloudkit.com/ck/2/cloudkit.js">
    > ```

    — https://developer.apple.com/documentation/cloudkitjs
* [tsl-apple-cloudkit exists on typescriptlibs.org](https://typescriptlibs.org/tsl-apple-cloudkit/), but the source is untrustworthy.
* [Questions for “cloudkit” and “javascript” on stackoverflow.com](https://stackoverflow.com/questions/tagged/cloudkit+javascript) don't yield many results (similar for [“cloudkit-js”](https://stackoverflow.com/search?q=cloudkit-js) and [“cloudkit-web-services”](https://stackoverflow.com/questions/tagged/cloudkit-web-services))
