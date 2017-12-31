# \<ajp-disqus-comments\>

Disqus web component for comments

## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

## Specific Setup

You must place `<div id="disqus_thread"></div>` in your root index page since the `embed.js` file that is imported is not able to look through layers in the DOM.

You may pass this as a template. From your root page, ie `index.html`:

```
<my-app><div id="disqus_thread"></div></my-app>
```

In `my-app.html` place `<slot></slot>` where you want the disqus thread to show up. You may place this as a template in another element and repeat the process.

I have it go up all the way to this component:

```
<ajp-disqus-comments subdomain="yoursubdomain"><slot></slot></ajp-disqus-comments>
```

For more information see [upgrade](https://www.polymer-project.org/2.0/docs/upgrade#replace-content-elements)

For this element, `ajp-disqus-comments`, place where you want it to show up and remember to import the component:

```
<link rel="import" href="../bower_components/ajp-disqus-comments/ajp-disqus-comments.html">
```

## Viewing Your Element

```
$ polymer serve
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.
