# Front End Ideas

## Intro
Using a new front end framework provides the opportunity to reconsider the architecture of our frontend. The following should be considered:
* Documentation
* Speed
* Testing
* Code modulation
* Code maintainability
* Code readability
* Code flexibility
* Code standards (linter/beautify)
* Best practices
* On boarding process for new developers
* Environment setup

To do this I have composed this file to serve as a guide/starting point with some ideas and technologies.

- - - -

## React
* [Redux](https://github.com/reactjs/redux) - Predictable state container for JavaScript apps. ([Probably unnecessary at this stage](https://medium.com/@dan_abramov/you-might-not-need-redux-be46360cf367))
* Mobile apps using [React Native](https://facebook.github.io/react-native/)
### Testing 
* [Jest](https://facebook.github.io/jest/) - with [Enzyme?](https://www.npmjs.com/package/enzyme)
    * [How to test react apps](https://medium.freecodecamp.org/the-right-way-to-test-react-components-548a4736ab22)
- - - -

## NPM
Use [npm](https://www.npmjs.com/) to manage front end dependencies.


* [Snyk](https://www.npmjs.com/package/snyk) detects vulnerabilities in dependencies (There is pricing involved)
* [Unpkg](https://unpkg.com/) is a cdn for npm packages (probably unnecessary)

**Note** - Each terminal, including production servers, will require node to be installed. However, this won't take long and wouldn't present issues in the future provided we use a node version manager or docker.

- - - -

## Build Tasks
* [npm scripts](https://www.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/)
* [Gulp](https://github.com/gulpjs/gulp) 
* [Grunt](https://github.com/gruntjs/grunt)

- - - -

## Css

* [Guidelines](https://cssguidelin.es/) - maybe collaborate and create our own style guide (The General rules section is a short summary)
    * [Architectural Principles](ttps://cssguidelin.es/#architectural-principles)
* [Css Stats](http://cssstats.com/)

### Browser Compatibility
* Achieve cross browser consistency with [normalize.css](https://github.com/necolas/normalize.css/)
* [Can I Use](https://caniuse.com)
* [Browser Shots](https://browsershots.org/)

### Preprocessors
* [Sass](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
* [PostCss](http://postcss.org/)
* [PostCss Parts](https://www.postcss.parts/) - A searchable catalog of PostCSS plugins
* https://developer.mozilla.org/en-US/docs/Glossary/CSS_preprocessor

### Media Queries
* media queries - [why-you-dont-need-device-specific-breakpoints](https://responsivedesign.is/articles/why-you-dont-need-device-specific-breakpoints/)
* [Top 14 Desktop, Mobile & Tablet Screen Resolutions](http://gs.statcounter.com/#desktop+mobile+tablet-resolution-ww-monthly-201608-201610-bar)

### Other
* [Flexbox](https://philipwalton.github.io/solved-by-flexbox/)
* [BEM Syntax](https://en.bem.info/)
    * https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/
* [Object oriented css](https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/)
* [Colection of Css libraries](https://github.com/ikkou/awesome-css)
* [Bootstrap Framework](https://hackerthemes.com/bootstrap-cheatsheet/)
* [PureCss Framework](https://purecss.io/)

## Js
* [Lodash](https://lodash.com) (A modern JavaScript utility library delivering modularity, performance & extras)

- - - -

## Testing

* [Guidelines](https://www.htmlgoodies.com/beyond/webmaster/guidelines-for-testing-front-end-web-components.html) to frontend testing
* [Introduction](https://www.creativebloq.com/how-to/an-introduction-to-frontend-testing) to frontend testing

### Js
* [Karma](https://github.com/karma-runner/karma) with [Jasmin](https://github.com/jasmine/jasmine) framework
* [Mocha](https://mochajs.org/)
* [Closure Compiler](https://developers.google.com/closure/compiler/)
* Remove unused js with [uglify's](https://github.com/mishoo/UglifyJS2/tree/harmony) dead_code option
* [ESLint](https://github.com/eslint/eslint)
* Error tracking with [Sentry](https://sentry.io/for/javascript/)

### Css
* Visual regression testing with [PhantomCSS](https://github.com/HuddleEng/PhantomCSS)
* Detect unused css with [PurifyCss](https://github.com/purifycss/purifycss)
* [Specificity Visualiser](https://francescoschwarz.de/en/blog/introducing-the-specificity-visualizer/)
* [Syntax validator](https://jigsaw.w3.org/css-validator/)
* [CSSLint](https://github.com/CSSLint/csslint)

**Note** - PhantomCss is no longer maintained but another solution is to use [headless chrome](https://developers.google.com/web/updates/2017/04/headless-chrome) with [resemble.js](https://github.com/Huddle/Resemble.js). [Puppeteer](https://github.com/GoogleChrome/puppeteer) may also be useful.

### Cross browser testing
* [Selenium](https://www.npmjs.com/package/selenium-webdriver)
* [Webdriver](https://w3c.github.io/webdriver/)
* [Headless chrome](https://developers.google.com/web/updates/2017/04/headless-chrome)


### HTML
* [Linter](https://github.com/mozilla/html5-lint)
* [Online syntax validator](https://validator.w3.org/)
* [Spell Checker](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/spellcheck)



- - - -

## Accessibility
* [Checklist](https://a11yproject.com/checklist.html)
* Use [Lighthouse](https://github.com/GoogleChrome/lighthouse) in chrome audits developer tools tab
* Readability of page https://www.webpagefx.com/tools/read-able/
* Color blind filters https://www.toptal.com/designers/colorfilter https://michelf.ca/projects/sim-daltonism/

- - - -

## General Development
* Code review process
* Limit size of certain files (400 Lines)
* Limit line length. (x chars)
* Limit function size (75 Lines)
* Detailed error handling: reduce debug/issue resolution times
* Complete separation of front and backend. Back end developers shouldn't have to touch the front end, and if they do, it should be code reviewed
* [Sentry sdk (raven.js)](https://docs.sentry.io/clients/javascript/)


### Source Control
* Use a branching strategy with different environments

eg

| Main (Production)  |
| ------------- |
| ^ | 
| UAT |
| ^ |
| Dev |
| ^ |
| Feature 1,  Feature 2...|



- - - -

## PWA
We can use the guidelines for the creation of a progressive web app. More info can be found here
https://developers.google.com/web/progressive-web-apps/ 
https://developers.google.com/web/progressive-web-apps/checklist
https://codelabs.developers.google.com/codelabs/your-first-pwapp/#0
Even if the development of a full progressive web app is infeasible (which it probably is), we can still use the tools available. For example [Lighthouse](https://github.com/GoogleChrome/lighthouse)

## Speed
Speed is king! 
https://developers.google.com/web/progressive-web-apps/
53% of users will abandon a site if it takes longer than 3 seconds to load! And once loaded, users expect them to be fast—no janky scrolling or slow-to-respond interfaces. 

A new architecture provides the opportunity to implement strategies and best practices to decrease loading times in the browser. 

More information found here https://developers.google.com/speed/docs/insights/about

Other useful links
* https://developers.google.com/closure/compiler/
* https://elliotec.com/how-to-get-100-google-page-speed-score/

- - - -


## Links
* https://www.sitepoint.com/javascript-modules-bundling-transpiling/
* http://2ality.com/2014/09/es6-modules-final.html
* https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript#parser-blocking-vs-asynchronous-javascript
* https://developers.google.com/web/fundamentals/performance/critical-rendering-path/page-speed-rules-and-recommendations
* https://developers.google.com/web/fundamentals/design-and-ux/responsive/
* https://developers.google.com/web/fundamentals/architecture/app-shell
* http://blog.88mph.io/2017/07/28/understanding-service-workers/
* https://jakearchibald.com/2014/offline-cookbook/
* https://www.reddit.com/r/webdev/comments/4nkcgv/chrome_service_worker_progressive_web_apps_how/
* https://developers.google.com/web/tools/setup/
* https://developers.google.com/web/fundamentals/design-and-ux/responsive/
* https://www.doubleclickbygoogle.com/articles/mobile-speed-matters/