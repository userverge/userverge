---
layout: article
title: "How to Control WebViews in your Electron App"
category: Electron
permalink: /electron/how-to-control-webviews-in-your-electron-app/
githublink: https://github.com/userverge/userverge/_post/electron/webview/2021-10-12-adding-controls.md
---

<div class="authors">
    <p>Author: <a href="https://github.com/KorbsStudio/" target="_blank">{% avatar KorbsStudio %} KorbsStudio</a></p>
</div>

We'll learn how to add functions to your Electron app that allows you and the user, if needed, to control the webview. Just like a modern web browser there are controls in the top area of the browser UI that lets you do actions like go back, go forward, refresh the page, and more. For now, we're going to add a back, forward, and refresh button.

Assuming you already have your Electron app setup, we need to add a configuration under `BrowserWindow` in our main process. You'll need to enable the `webviewTag` API like this:
```js
...
    webPreferences: {
        webviewTag: true
    }
...
```

Then we can add a webview to the <u>index.html</u> for us to control later. We'll need to also give it an `id` name so we can identity the webview in our functions to control it:
```html
<webview id="primary" src="https://userverge.com/"></webview>
```

While we're adding that, let's add our buttons with functions we will setup soon:
```html
<div class="controls">
    <buttons onclick="PrimaryGoBack();">Go back</button>
    <buttons onclick="PrimaryGoForward();">Go forward</button>
    <buttons onclick="PrimaryRefresh();">Refesh</button>
</div>
```

Then we'll add a file to put our functions in and name it <u>webview-controls.js</u>. We'll use `var` to indentity each webview we use in the app:
```js
var primary = document.getElementById('primary')

function PrimaryGoBack() {primary.goBack();}
function PrimaryGoForward() {primary.goForward();}
function PrimaryRefresh() {primary.reload();}
```

Simply star the app and try out the controls.

#### Also look at:
[https://www.electronjs.org/docs/latest/api/webview-tag](https://www.electronjs.org/docs/latest/api/webview-tag)