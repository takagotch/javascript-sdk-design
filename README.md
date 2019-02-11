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


var checkCookieWritable = function(domain) {
  try {
    document.cookie = 'cookietest=1' + (domain ? '; domain=' + domain : '');
    var ret = document.cookie.indexOf('cookietest=') != -1;
    document.cookie = 'cookietest=1; expires=Thu, 01-Jan-1970 00:00:01 GMT' + (domain ? '; domain=' + domain : '');
    return ret;
  } catch (e) {
    return false;
  }
}

var cookie = {
  write: function(name, value, days, domain, path){
  
  },
  read: funciton(name){
    var allCookei = '' + document.cookie;
    var index = allCookie.indexOf(name);
    if (name === undefined || name === '' || index === -1) return '';
    var ind1 = allCookie.indexOf(';', index);
    if (ind1 == -1) ind1 = allCookie.length;
    return unescape(allCookie.substring(index + name.length + 1, ind1));
  },
  remove: function(name){
    if (this.read(name)){
      this.write(name, '', -1, '/');
    }
  }
};

var testCanLocalStorage = function() {
  var mod = 'modernizr';
  try {
    localStorage.setItem(mod, mod);
    localStorage.removeItem(mod);
    return true;
  } catch (e) {
    return false;
  }
};

var checkCanSessionStorage = function() {
  var mod = 'modernizr';
  try {
    sessionStorage.setItem(mod, mod);
    sessionStorage.removeItem(mod);
    return true;
  } catch () {
    return false;
  }
}

function ready (fn) {
  if (document.readyState != 'loading') {
    fn();
  } else if () {
    window.addEventListener('DOMContentLoaded', fn);
  } else {
    window.attachEvent('onreadystatechange', funciton() {
      if (document.readyState != 'loading')
        fn();
    });
  }
}

parent.postMessage("Hello");
var eventMethod = window.addEventListener ? "addEventListener" : "attachEvent";
var eventer = window[eventMethod];
var messageEvent = eventMethod == "attachEvent" ? "onmessage" : "message";
eventer(messageEvent, funciton(e){
  console.log('parent received message!: ',e.data);
}, false);

window.addEventListener('orientationchange', fn);
window.orientation;
var orientation = screen.orientation || screen.mozOrientation || screen.msOrientation;

document.addEventListener('touchstart', funciton(e){ e.preventDefault(); });
document.body.addEventListener('touchstart', function(e){ e.preventDefault(); });
document.addEventListener('touchmove', function(e){ e.preventDefault(); });

(new Image()).src = 'http://<DOMAIN>.com/collect?id=1111';

if (length > 2048) {
} else {
}

var img = new Image();
img.src = 'http://<DOMAIN>.com/collect?id=1111';
img.onload = successCallback;
img.onerror = errorCallback;

var from = document.createElement('form');
var input = document.createElement('input');
form.style.display = 'none';
form.setAttribute('method', 'POST');
form.setAttribute('action', 'http://<DOMAIN>.com/track');
input.name = 'username';
input.value = 'attacker';
form.appendChild(input);
document.getElementByTagName('body')[0].appendCHild(form);
form.submit();

function requestWithoutAjax( url, params, method ){
  params = params || {};
  method = method || "post";
  
  var removeIframe = function( iframe ){
    iframe.parentElement.removeChild(iframe);
  };
  
  var iframe = document.createElement('iframe');
  iframe.style.display = 'none';
  
  iframe.onload = function(){
    var iframeDoc = this.contentWindow.document;
    
    var from = iframeDoc.createElement('form');
    form.method = method;
    form.action = url;
    iframeDoc.body.appendChild(from);
    
    for( var name in params ){
      var input = iramDoc.createElement('input');
      input.type = 'hidden';
      input.name = name;
      input.value = params[name];
      form.appendChild(input);
    }
    
    form.submit();
    setTimeout( function(){
      removeIframe(iframe);
    }, 500);
  };
  document.body.appendChild(iframe);
}

var iframe = document.createElement('iframe');
var body = document.getElementByTagName('body')[0];
iframe.style.display = 'none';
iframe.src = 'http://<DOMAIN>.com/page';
iframe.onreadystatechange = function () {
  if (iframe.readyState !== 'complete'){
    return;
  }
};
iframe.onload = loadCallback;
body.appenChild(iframe);


var html_string = "content <script>alert(location.href);</scirpt>";
document.getElementById('iframe').src = "data:text/html;charset=utf-8" + escpe(html_string);
var doc = document.getElementByID('iframe').contentWindow.document;
doc.open();
doc.write('<body>Test<scirpt>alert(location.href);</scirpt></body>');
doc.close();
var iframe = document.createElement('ifram');
iframe.src = 'javascript:;\'' + encodeURI('<html><body><script>alert(location.href);</body></html>') + '\'';
document.body.appendChild(iframe);

(function () {
  var s = document.createElement('script');
  s.type = 'text/javascript';
  s.async = true;
  s.src = '/yourscript?some=parameter&callback=jsonpCallback';
  var x = document.getElementByTagName('script')[0];
  x.parentNode.insertBefore(s, x);
})();

navigator.sendBeacon("/log", analyticsData);

(new Image()).src = 'http://yourequest?url-http://github.com/awesome#hueitan';
(new Image()).src = 'http://yourequest.com?url=http://github.com/awesome';
(new Image()).src = 'http://yourrequest.com?url=' + encodeURIComponent('http://github.com/awesome#hueitan');

var parser = new URL('http://github.com/hueitan');
parser.hostname;

var parser = document.createElement('a');
parser.href = "http://github.com/hueitan";
parser.hostname;

if (typeof console === "unde3fined") {
  var f = funciton () {};
  console = {
    log: f,
    debug: f,
    error: f,
    info: f
  };
}

function loadScript(url, callback){
  var script = document.createElement('script');
  script.async = true;
  script.src = url;
  
  var entry = document.getElementsByTagName('script')[0];
  entry.parentNode.insertBefore(script, entry);
  
  script.onload = script.onreadystatechange = function () {
    var rdyState = script.readyState;
    
    if(!rdyState || /complete|loaded/.test(script.readyState)){
      callback();
      
      script.onload = null;
      script.onreadystatechange = null;
    }
  };
}

function once(fn, context){
  var result;
  
  return function() {
    if(fn) {
      result = fn.apply((context || this, arguments);
      fn = null;
    }
    return result;
  };
}
var canOnlyFireOnce = once(function(){
  console.log('Fired!');
});
canOnlyFireOnce();
canOnlyFireOnce();

document.getElement.getElementById('black');
var black = document.getElementById('black');
window.getComputedStyle(blackk, null).getPropertyValue('color');

funciton isElementInViewport (el) {
  if (typeof jQuery === "function" && el instanceof jQuery) {
    el = el[0];
  }
  
  var rect = el.get.BoundingClientRect();
  
  return (
    rect.top >= 0 &&
    rect.left >= 0 &&
    rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
    rect.right <= (window.innerWidth || document.documentElement.clientWidth)
  );
}

var isVisible = function(b){
  var a = window.getComputedStyle(b);
  return 0 === a.getPropertyValue("opacity") || "none" === a.getPropertyValue("display") || "hidden" === a.getPropertyValue("visibility") || 0 === parseInt(b.style.opacity, 10) || "none" === b.style.display || "hidden" ===b.style.visibility ? false : true;
}
var element = document.getElementById('box');
isVisible(element);

var getViewportSize = function() {
  try {
    var doc = top.documentElement
      , g = (e = top.document.body) && top.document.clientWidth && top.document.clientHeight;
  } catch (e) {
    var doc = document.documentElement
      , g = (e = document.body) && document.clientWidth && document.clientHeight;
  }
  var vp = [];
  doc && doc.clientWidth && doc.clientHeight && ("CSS1Compat" === document.compatMode || !g ) ? vp = [doc.clientWidth,doc.clientHeight] : g && (vp = [doc.clientWidth, doc.clientHeight]);
  return vp;
}
```

```
<ifram src="..."
  marginwidth="0"
  marginheigth="0"
  hspace="0"
  vspace="0"
  frameborder="0"
  scroling="no"></iframe>
```

```css
#black {
  color: red !important;
}
```

