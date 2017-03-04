# Progressive Web Apps
Playground for learning about PWA development.

##Meetup
Speaker: Enrique García Navalón (@garcianavalon)
Slides: 
* https://speakerdeck.com/garcianavalon/progressive-web-apps-que-son-como-se-hacen-y-por-que-deberian-importarte
* https://speakerdeck.com/garcianavalon/progressive-web-apps-for-mobile-developers

**Characteristics**
* Reliable
* Fast
* Engaging

**Technologies involved**
 * Responsive CSS
 * Service Workers
    * https://developers.google.com/web/fundamentals/getting-started/primers/service-workers
    * Service workers tutorial: https://codelabs.developers.google.com/codelabs/debugging-service-workers/#0
 * Web Push Notifications
    * https://developers.google.com/web/fundamentals/engage-and-retain/push-notifications/
    * Example: https://github.com/GoogleChrome/samples/tree/gh-pages/push-messaging-and-notifications

**Architecture and Design principles**
* offline-first
* Appshell
    * The app's shell is the minimal HTML, CSS, and JavaScript that is required to power the user interface of a progressive web app and is one of the components that ensures reliably good performance. Its first load should be extremely quick and immediately cached. "Cached" means that the shell files are loaded once over the network and then saved to the local device. Every subsequent time that the user opens the app, the shell files are loaded from the local device's cache, which results in blazing-fast startup times.
* Optimize performance

**Examples**
* Twitter mobile site (React PWA)
    * https://www.infoq.com/news/2017/02/twitter-react-mobile-stack?utm_source=twitter&utm_campaign=calendar&utm_medium=link
* Telegram web based
* Alibaba

**Tools**
* Lighthouse audit tools:
    * https://developers.google.com/web/tools/lighthouse/
* App Manifest generator


##Interesting links
* https://developers.google.com/web/progressive-web-apps/
* https://pwa.rocks
* http://offlinefirst.org
* PWA Checklist: https://developers.google.com/web/progressive-web-apps/checklist
* Web Starter Kit: https://developers.google.com/web/tools/starter-kit/


##Tutorial from Google
https://codelabs.developers.google.com/codelabs/your-first-pwapp/#0

1. Download source code
2. Install Web server for Chrome: https://goo.gl/IoEaMq
3. Point to the work folder and test it works: http://127.0.0.1:8887/
4. Test with fake data
5. Start with a fast first load
    * User preferences, like the list of cities a user has subscribed to, should be stored locally using IndexedDB or another fast storage mechanism. To simplify this code lab as much as possible, we've used localStorage, which is not ideal for production apps because it is a blocking, synchronous storage mechanism that is potentially very slow on some devices.
    * https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage
    * Extra Credit: Replace localStorage implementation with idb, check out localForage as a simple wrapper to idb.
    * https://github.com/localForage/localForage
6. Use service workers to pre-cache the App Shell:
    * Service worker functionality is only available on pages that are accessed via HTTPS (http://localhost and equivalents will also work, to facilitate testing). To learn about the rationale behind this restriction check out Prefer Secure Origins For Powerful New Features from the Chromium team.
    * Register the service worker if it's available
    * Cache the site assets
    * Serve the app shell from the cache
    * Beware of the edge cases: use something like https://github.com/GoogleChrome/sw-precache
7. TBD  