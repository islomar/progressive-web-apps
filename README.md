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
3. 