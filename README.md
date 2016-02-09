# ServiceWorker Cheat Sheet

A CheatSheet containing getting started, tips, tricks, best practices, code and more about ServiceWorker.

![Cheat Sheet](http://i.imgur.com/BpAPJtX.jpg)

## Reference

* [Service Worker Cookbook](https://serviceworke.rs/)
* [Introduction to Service Worker](http://www.html5rocks.com/en/tutorials/service-worker/introduction/)
* [The offline cookbook](https://jakearchibald.com/2014/offline-cookbook/)
* [Using Service Workers today](https://jakearchibald.com/2014/using-serviceworker-today/)

### What is ServiceWorker?

ServiceWorker is a background worker, it gives us a JavaScript context to add features such as push messaging, background sync, geofencing and network control.

### Getting Started

To begin, you need to register for a ServiceWorker from your page:

```javascript
if ('serviceWorker' in navigator) {
  navigator.serviceWorker.register('/worker.js').then(function(reg) {
    console.log('😃', reg);
  }, function(err) {
    console.log('😭', err);
  });
}
```

As you can see, `.register` take a URL for your worker script and returns a promise. The ServiceWorker script must be on the same origin as your page.
