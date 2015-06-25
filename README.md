
### Quick start
```bash
$ npm start # then open your browser and go to http://localhost:8080
```


## File Structure
We use the component approach in our starter. This is the new standard for developing Angular apps and a great way to ensure maintainable code by encapsulation of our behavior logic. A component is basically a self contained app usually in a single file or a folder with each concern as a file: style, template, specs, e2e, and component class. Here's how it looks:
```
angular2-webpack-starter/
 ├──public/                           * static assets are served here
 │   ├──lib/                          * static libraries
 │   │   └──traceur-runtime.min.js    * ignore this file. This is needed to polyfill the browser to for ES6 features to similarly
 │   │
 │   ├──favicon.ico                   * replace me with your own favicon.ico
 │   ├──service-worker.js             * ignore this. Web App service worker that's not complete yet
 │   ├──robots.txt                    * for search engines to crawl your website
 │   ├──human.txt                     * for humans to know who the developers are
 │   │
 │   └──index.html                    * Index.html: where we place our script tags
 │
 ├──src/                              * our source files that will be compiled to javascript
 │   ├──app/                          * WebApp folder
 │   │   ├──bootstrap.ts              * entry file for app
 │   │   │
 │   │   ├──components/               * where most of components live
 │   │   │   ├──todo.ts               * an example of a component using a service and forms
 │   │   │   ├──dashboard.ts          * a simple Component with a simple Directive example
 │   │   │   │
 │   │   │   ├──home/                 * example component as a folder
 │   │   │   │   ├──home.ts           * how you would require your template and style files
 │   │   │   │   ├──home.css          * simple css file for home styles
 │   │   │   │   └──home.html         * simple html file for home template
 │   │   │   │
 │   │   │   └──app.ts                * App.ts: entry file for components
 │   │   │
 │   │   ├──services/                 * where we keep our services used throughout our app
 │   │   │   ├──TodoService.ts        * an example of a simple service 
 │   │   │   └──services.ts           * where we gather our injectables from our services
 │   │   │
 │   │   └──directives/               * where we keep our directives used throughout our app
 │   │       ├──Autofocus.ts          * another simple directive to fix a problem with the router
 │   │       └──directives.ts         * where we gather our directives from our directives
 │   │
 │   └──common/                       * where common files used throughout our app
 │       ├──shadowDomInjectables.ts   * determind if the user is on chrome and use ShadowDom
 │       ├──jitInjectables.ts         * turn on Just-In-Time Change Detection
 │       ├──formInjectables.ts        * services exported by angular/forms which is the FormBuilder
 │       └──BrowserDomAdapter.ts      * ignore this. we need to set the DomAdapter to the browser
 │
 ├──typings/                          * where tsd defines it's types definitions
 │   ├──_custom/                      * where we define our custom types
 │   │   ├──ng2.d.ts                  * where we patch angular2 types with our own types until it's fixed
 │   │   └──custom.d.ts               * we include all of our custom types here
 │   │
 │   ├──angular2/
 │   │   └──angular2.d.ts             * our Angular 2 type definitions
 │   │
 │   ├──es6-promise/
 │   │   └──es6-promise.d.ts          * ES6 promises type definitions
 │   │
 │   ├──rx/
 │   │   ├──rx-lite.d.ts              * rx-lite type definitions
 │   │   └──rx.d.ts                   * rx type definitions
 │   │
 │   └──tsd.d.ts.ts                   * our main file for all of our type definitions
 │
 ├──tsconfig.json                     * config that webpack uses for typescript
 ├──tsd.json                          * config that tsd uses for managing it's definitions
 ├──package.json                      * what npm uses to manage it's dependencies
 └──webpack.config.js                 * our webpack config
```

# Getting Started
## Dependencies
What you need to run this app:
* `node` and `npm` (`brew install node`)
* Ensure you're running the latest versions Node `v0.12.2`+ and NPM `2.10.0`