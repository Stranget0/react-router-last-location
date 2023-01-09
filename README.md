# react-router-last-location-17
## [Original](https://www.npmjs.com/package/react-router-last-location)

This is just a copy to fix peer dependency issues

- Provides access to the last location in `react` + `react-router (v4.x, v5.x)` applications.
- ❤️ Using [`hooks`](https://reactjs.org/docs/hooks-overview.html)? If yes, `useLastLocation`.
- 💉 Using [`HOC`](https://reactjs.org/docs/higher-order-components.html)? - If yes, `withLastLocation`.
- Handle redirects.
- Support ![TypeScript](https://user-images.githubusercontent.com/1313605/53197634-df9a6d00-361a-11e9-81ba-69f8a941f8a2.png)
- Useful for handling internal routing.
- Easily keep your users inside your app.

## Note: Last location != Previous browser history state

This library only returns the location that was active right before the recent location change, during the lifetime of the current window.

This means, it is not equal to the "location you were at before navigating to this history state".

In other words, the location this library provides is not necessarily the same as the one when you click the browser's back button.

**Example 1**

1. Visit `/`: last location = `null`, previous browser history state = `null`
2. Visit `/a`: last location = `/`, previous browser history state = `/`
3. Visit `/b`: last location = `/a`, previous browser history state = `/a`
4. Reload (url will stay at `/b`): last location = `null`, previous browser history state = `/a`

**Example 2**

1. Visit `/`: last location = `null`
2. Visit `/a`: last location = `/`
3. Visit `/b`: last location = `/a`
4. Go back: last location = `/b`, previous browser history state = `/`

**Example 3**

1. Visit `/`: last location = `null`
2. Visit `/a`: last location = `/`
3. Visit `/b`: last location = `/a`
4. Visit `/c`: last location = `/b`
4. Go back to `/a` (by selecting that state explicitly in "Go back" browser dropdown that is visible upon clicking it with right mouse button): last location = `/c`, previous browser history state = `/`

## How to use?

```bash
# Please remember that you should have installed react, prop-types and react-router-dom packages
# npm install react prop-types react-router-dom --save

npm install react-router-last-location-17 --save
```
