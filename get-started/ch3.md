## Chapter 3: Digging into App Platform

The intent of this chapter is to give the you an mental model of an Freshworks App and how that plays on the app Platform. Before you can move forward, it is recommended that you have explored and tried out building any simple app from the documentation. While you are at it, this part of the guide requires you to be read alongside any App SDK documentation of Freshworks Product.

There are 3 main components that you'd need to keep in perspective while trying ot understand Freshworks App Platform.

1. Client-side
2. Configuration
3. Serverless

An ideal Freshworks App directory

```bash
├── app
│   ├── index.html
│   ├── scripts
│   │   └── app.js
│   └── styles
│       ├── images
│       │   ├── icon.svg
│       │   └── rocket.svg
│       └── style.css
├── config
|   |-- oauth_config.json
|   |-- assets/iparams.js
│   └── iparams.json / iparams.html
├── manifest.json
├── server
    └── server.js
```

### Client Side Components

App renders in an `<iframe>` . The frontend files such as HTML, CSS and JS files will run by Browser and UI of the app is rendered.

**app{}**

The Freshworks product is a single page SaaS application. Depending on the placeholders where the app chooses to be rendered UI components in the foreground or just JS in background, platform gives control to you.

1. As soon as user hits Freshworks product portal URL for the first time, platform sends app's clientside components like HTML,CSS and JS to the browser.
2. The Javascript thread of execution will weave in the order you mention `<script>` and `<link>` css.
3. If app's Javascript has
    1. `app.initialized()` - It returns a promise where you can pass an callback function. It happens first time when Freshworks product loads.
    2. `app.activated()` and `app.deactivated()` are similar accepts a callback function as argument, but they are invoked based on app placeholder.

**client{}**

Just like your JS scope has access to `app`, `app.initialized()` returns a promise to which your callback function will have access to an `client` object. This allows your app to be able to invoke any platform features mentioned in the Infrastructure.

1. `client.data.get("<argument>")` - returns a promise where your callback would have access data in the page which user is currently viewing.
2. `client.events.on("<argument>", callback)` - takes in a callback which will be invoked when desired event occured.
3. `client.interface.trigger("<argument>", { "key": "value" })` - gives the app access to show a notficiation, modal, so on.
4. `client.db.METHOD("KEY", "VALUE"[,options])` - gives app the persist key value pairs.
5. `client.request.METHOD("URL", options)` - returns a promise resolves with a callback which gives access to response payload in the callback's scope. This how your app can make API calls from the client side.
6. `client.instance.METHOD()` - returns a promise where you can pass callback or it simply invokes a method. Either case, whenever you have mulitple placeholders used by the same app, you can pass the contextual data from one placeholder to another maintaining it's state.

**OAuth**

If app needs talk to 3rd party, you'll need to add `oauth_config.json` file with all the necessary information. This will leave the app user to perform OAuth2.0 handshake first and then use the app. Platform would handle all the token management on behalf of you.

### Configuration Page

This page is rendered when app tries to install in an account. App platform has a way to ease up this building an installation/configuration page. It is by using

1. `iparams.json`
2. or `iparams.html`

App would generally requires some details from the user to happen to be installed. For example, it will have to store an API key in order to make API calls later on. Any of `iparams.json` or `iparams.html` would

This is not a tutorial. All the resources that you may need, I will add them in Appendix B.
