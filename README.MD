Use this Polymer element to easily add Google Analytics to a Polymer application that is using [app-router](https://github.com/erikringsmuth/app-router).

**Note:** Currently requires a fork of app-router to be able to listen to the correct event. [app-router fork](https://github.com/rurri/app-router). This requirement will be removed once a pull request is accepted or another feasible way to subscribe to these events is published.

To use, just insert this element anywhere in your page (Usually is placed at the end of the body tag)

```
<app-router-analytics trackingId="UA-1234567890-1"></app-router-analytics>
```

Default behavior will report the url to Google Analytics with a hash as the URL. For the internal route of /blog, it is reported as /#/blog.

This is configurable with the `mode` otpion.

Options are:

* hash: will be reported as /#/blog
* hashbang, reported as /#!/blog
* raw, reported as /blog

This is an optional attribute and can be set on the element when created:

```
<app-router-analytics trackingId="UA-1234567890-1" mode="hashbang"></app-router-analytics>
```