---
title: "how to set up a @vercel #react #next project to use a @google global site tag (@google analytics) #webdev #seo"
date: 2020-12-21
categories: 
  - "fsse"
---

how to set up a @vercel #react #next project to use a @google global site tag (@google analytics) #webdev #seo

simple usage

- set a vercel env var GTAG to your google tag id
- add /pages/\_document.js to your project

/pages/\_document.js

```jscript
import Document, { Html, Head, Main, NextScript } from 'next/document'

export default class MyDocument extends Document {
  render() {
    var gtag = process.env.GTAG
    return (
      <Html>
        <Head>
          {/* Global Site Tag (gtag.js) - Google Analytics */}
          <script
            async
            src={`https://www.googletagmanager.com/gtag/js?id=${gtag}`}
          />
          <script
            dangerouslySetInnerHTML={{
              __html: `
            window.dataLayer = window.dataLayer || [];
            function gtag(){dataLayer.push(arguments);}
            gtag('js', new Date());
            gtag('config', '${gtag}', {
              page_path: window.location.pathname,
            });
          `,
            }}
          />
        </Head>
        <body>
          <Main />
          <NextScript />
        </body>
      </Html>
    )
  }
}
```

advanced google site tag pageviews and events usage

- [Analytics (google.com)](https://analytics.google.com/analytics/web)
- [Add gtag.js to your site  |  Universal Analytics for Web (gtag.js) (google.com)](https://developers.google.com/analytics/devguides/collection/gtagjs)
- [Measure pageviews  |  Universal Analytics for Web (gtag.js) (google.com)](https://developers.google.com/analytics/devguides/collection/gtagjs/pages)
- [Measure Google Analytics Events](https://developers.google.com/analytics/devguides/collection/gtagjs/events)
- [Using Google Analytics with Next.js | hoangtrinhj.com](https://hoangtrinhj.com/using-google-analytics-with-next-js)
- [javascript - How to use google analytics with next.js app? - Stack Overflow](https://stackoverflow.com/questions/60411351/how-to-use-google-analytics-with-next-js-app)

google site tag & google analytics statistics

<figure>

[![](https://fsse8info.wordpress.com/wp-content/uploads/2020/12/screenshot-analytics.google.com-2020.12.21-01-30-36.png?w=885)](https://fsse8info.wordpress.com/wp-content/uploads/2020/12/screenshot-analytics.google.com-2020.12.21-01-30-36.png)

<figcaption>

realtime map of locations of users

</figcaption>

</figure>
