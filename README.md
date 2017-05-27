# \<ga-dnt-analytics\>

Basic Google Analytics web component with Do Not Track support. [![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/justinribeiro/ga-dnt-analytics)


<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="ga-dnt-analytics.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<ga-dnt-analytics debug="true"></ga-dnt-analytics>
ga-dnt-analytics - Open DevTools and check console.
```

![image](https://cloud.githubusercontent.com/assets/643503/22002837/e9e55dd8-dc03-11e6-8f3b-147be85ae76f.png)

## Installation

Install the component using Bower:

```shell
bower i justinribeiro/ga-dnt-analytics --save
```

## Usage

1. Import Web Components' polyfill, if needed:

    ```html
    <script src="bower_components/webcomponentsjs/webcomponents-loader.js"></script>
    ```

2. Import ga-dnt-analytics:

    ```html
    <link rel="import" href="bower_components/ga-dnt-analytics/ga-dnt-analytics.html"/>
    ```

3. Start using it!

    ```html
    <ga-dnt-analytics key="UA-XXXXXX-X"></ga-dnt-analytics>
    ```


## Attributes/Properties

Attribute | Options      | Default  | Description
---       | ---          | ---      | ---
`key`     | *String*     | ""       | (_optional_) Sets UA for Google Analytics tracking
`debug`   | *Boolean*    | `false`  | (_optional_) Enables Google Analytics debugging mode
`trace`   | *Boolean*    | `false`  | (_optional_) Use with debug; enables full tracing for GA
`donottrack` | *Boolean*  | `true`   | (_optional_) Check and use Do Not Track browser flag
`pageview`    | *Boolean*    | `false`   | (_optional_) Send `ga('send', 'pageview')` ping on element stamp

## Methods

If not using the `pageview` property to send a ping to GA, you can use the `send()` method to send a payload to GA.

```javascript
// via Polymer 2.x
this.$$('ga-dnt-analytics').send({
  hitType: 'pageview',
  page: window.location.pathname,
  location: window.location.href,
  title: 'My Title'
});

// via JavaScript
document.querySelector('ga-dnt-analytics').send({
  hitType: 'pageview',
  page: window.location.pathname,
  location: window.location.href,
  title: 'My Title'
});
```

For list of payloads and string/objects to send, see [See https://developers.google.com/analytics/devguides/collection/analyticsjs/sending-hits](https://developers.google.com/analytics/devguides/collection/analyticsjs/sending-hits).

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Credits

[Justin Ribeiro](https://github.com/justinribeiro)
[Schalk Neethling](https://github.com/schalkneethling)
[Google Analytics](https://developers.google.com/analytics/)

## License

MIT License (MIT)