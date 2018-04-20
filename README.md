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

Can be used with React Native with similar steps:
- Install using `npm install --save-dev measure-wasted-renders`
- Run your app and select "Debug JS Remotely" in the simulator.
- Select "debuggerWorker.js" in the Chrome console.
<img width="1440" alt="screen shot 2018-04-20 at 10 58 37 am" src="https://user-images.githubusercontent.com/7039196/39058641-6bd3477a-448a-11e8-88de-3f0405ec1a3d.png">


## TO DO
 - remove lodash dependency
 - publish to npm
 
