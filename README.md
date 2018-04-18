# measure-wasted-renders

**to install**

```bash
npm install --save-dev measure-wasted-renders
```

**to use**

```js
// in your app's entry-point
import React from "react";
import measureWastedRenders from "measure-wasted-renders";

if (process.env.NODE_ENV !== "production") {
  measureWastedRenders(React);
}
```

Then later inside the devtools console you can run `window.prettyPrintWasted()` which outputs a table describing all of the components that have rerendered based on shallow changes to its props that were actually deeply equal to previous props.

![](https://user-images.githubusercontent.com/4656974/35294060-a1affd1a-0043-11e8-88a8-3c6e291fff67.png)



## TO DO
 - remove lodash dependency
 - publish to npm