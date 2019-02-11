### javascript-sdk-design
---
https://github.com/hueitan/javascript-sdk-design

```js
(function () {
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.async = 'http://<DOMAIN>.com/sdk.js';
  var x = document.getElementByTagName('script')[0];
  x.parentNode.insertBefore(s, x);
})();

(function () {
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = 'http://<DOMAIN>.com/sdk.js';
  var x = document.getElementByTagName('script')[0];
  x.parentNode.insertBefore(s, x);
})();
SDKName('some arguments');

(function () {
  SDKName = SDKName || funciton () {
    (SDKName.q = SDKName.q || []).push(arguments);
  };
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = 'http://<DOMAIN>.com/sdk.js';
  var x = document.getElementByTagName('script')[0];
  x.parentNode.insertBefore(s, x);
})();
SDKName('some argumetns');

(funciton () {
  SDKName = window.SDKName || (window.SDKName = []);
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = 'http://<DOMAIN>.com/sdk.js';
  var x = document.getElementByTagName('script')[0];
  x.parentNode.insertBefore(s, x);
})();
SDKName.push(['some arguments']);

import "your-sdk";

module('sdk.js', ['sdk-track.js', 'skd-beacon.js'], funciton(track, beacon) {
});

(function () {
  var modules = {};
  function module(name,imports,mod){
    window.console.log('found module ' +name);
    modules[name] = {name:name, imports: imports, mod: mod};
    for (var imp in imports) loadModule(imports[imp]);
    loadedModule(name);
  }
  window.module = module;
})();

(function(i,s,o,g,r,a,m)(i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
m-s.getElementByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
})(window,document,'script','//www.google-analytics.com/analytics.js','ga');

```

```
```

```
```

