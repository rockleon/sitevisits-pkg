# @rockleon/site-visits

[![npm (scoped)](https://img.shields.io/npm/v/@rockleon/site-visits.svg)](https://www.npmjs.com/package/@rockleon/site-visits)
[![npm bundle size (minified)](https://img.shields.io/bundlephobia/min/@rockleon/site-visits.svg)](https://www.npmjs.com/package/@rockleon/site-visits)

**npm package to keep count of visits made to your website.**

Want to keep count of the number of times your website is viewed? Well, here's a solution!

Keep track of visit-count of all your websites. At one place!!

Website : [https://site-visits-rockleon.web.app/](https://site-visits-rockleon.web.app/)

Steps :
- Go to the specified website and register/login.
- Create a project for your specific website; a unique key will be generated.
- Use the key with this package.


## Install

Using npm
```
npm install @rockleon/site-visits
```
Using yarn
```
yarn add @rockleon/site-visits
```

## Usage

```js
// Import function from package
import updateSiteVisit from "@rockleon/site-visits";

// Execute function
const key = "your_key";
updateSiteVisit(key);
```

Import and call this function in the main page/app/index of your project in the following functions, so that the visit-count updates when your main page is loaded.
- Javascript: window.onload()
- React: componentDidMount()
- Vue: mounted()
- Angular: ngOnInit()

### Debug Mode
You can use this package in debug mode by passing the second argument as 'true' while developing and testing your site.
In debug mode, your website's actual visit count won't get updated.
Instead you will recieve messages in console informing whether the package is working fine; or stating the errors, if any.
If you are running the website locally, then the package will by default run in debug mode.

```js
const key = "your_key";
updateSiteVisit(key, true);
```

This package makes use of [SessionStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage) to prevent visit-count updates if the user refreshes or navigates in the same website. The visit-count is not updated if the browser doesn't support SessionStorage.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)