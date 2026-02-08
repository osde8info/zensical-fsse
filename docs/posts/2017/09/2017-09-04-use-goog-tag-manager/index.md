---
title: "use goog tag manager to manage your analytics and marketing tags and tracker scripts"
date: 2017-09-04
categories: 
  - "fsse"
tags: 
  - "analytics"
  - "goog"
  - "js"
  - "script"
  - "tags"
  - "tracking"
---

you can use goog tag manager to manage your analytics and marketing tags and tracker code by including one code snippet (the goog tag man js script and noscript code) that then includes all the other js scripts

- https://developers.google.com/tag-manager/
- https://developers.google.com/tag-manager/quickstart
- https://www.youtube.com/watch?v=7FXbsCWsEi8
- https://www.youtube.com/watch?v=KRvbFpeZ11Y

SCRIPT

```
(function(w,d,s,l,i){w[l]=w[l]||[];w[l].push({'gtm.start':
new Date().getTime(),event:'gtm.js'});var f=d.getElementsByTagName(s)[0],
j=d.createElement(s),dl=l!='dataLayer'?'&l='+l:'';j.async=true;j.src=
'https://www.googletagmanager.com/gtm.js?id='+i+dl;f.parentNode.insertBefore(j,f);
})(window,document,'script','dataLayer','GTM-XXXX');
```

NOSCRIPT

```
iframe src="https://www.googletagmanager.com/ns.html?id=GTM-5B8XWMR"
height="0" width="0" style="display:none;visibility:hidden"
```

or

```
a href="https://www.googletagmanager.com/ns.html?id=GTM-XXXX" https://www.googletagmanager.com/ns.html?id=GTM-XXXX a

```

see also

- http://www.lunametrics.com/blog/2017/01/26/install-google-tag-manager-on-wordpress/
- https://wpism.com/google-tag-manager-wordpress/
