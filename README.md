[![Svelte v3](https://img.shields.io/badge/svelte-v3-orange.svg)](https://svelte.dev)
[![npm](https://img.shields.io/npm/v/svelte-websocket-store.svg)](https://www.npmjs.com/package/svelte-websocket-store)
[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)
[![bundlejs](https://deno.bundlejs.com/?q=svelte-websocket-store\&badge=detailed)](https://bundlejs.com/?q=svelte-websocket-store)
[![downloads](http://img.shields.io/npm/dm/svelte-websocket-store.svg?style=flat-square)](https://npmjs.org/package/svelte-websocket-store)
[![GitHub Issues](https://img.shields.io/github/issues/arlac77/svelte-websocket-store.svg?style=flat-square)](https://github.com/arlac77/svelte-websocket-store/issues)
[![Build Status](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2Farlac77%2Fsvelte-websocket-store%2Fbadge\&style=flat)](https://actions-badge.atrox.dev/arlac77/svelte-websocket-store/goto)
[![Styled with prettier](https://img.shields.io/badge/styled_with-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![Known Vulnerabilities](https://snyk.io/test/github/arlac77/svelte-websocket-store/badge.svg)](https://snyk.io/test/github/arlac77/svelte-websocket-store)
[![Coverage Status](https://coveralls.io/repos/arlac77/svelte-websocket-store/badge.svg)](https://coveralls.io/github/arlac77/svelte-websocket-store)
[![Tested with TestCafe](https://img.shields.io/badge/tested%20with-TestCafe-2fa4cf.svg)](https://github.com/DevExpress/testcafe)

# svelte-websocket-store

Svelte store with a websocket backend

```js
import websocketStore from "svelte-websocket-store";

const initialValue = { };
export const myStore = websocketStore("wss://mydomain.com/ws1", initialValue, ['option 1', 'option 2']);


// send JSON to websocket server
$myStore = { content: "to be saved", other_values: "all" };


// receive JSON from server (push)
let response = $myStore;
```

# API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

*   [websocketStore](#websocketstore)
    *   [Parameters](#parameters)

## websocketStore

Create a writable store based on a web-socket.
Data is transferred as JSON.
Keeps socket open (reopens if closed) as long as there are subscriptions.

### Parameters

*   `url` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** the WebSocket url
*   `initialValue` **any** store value used before 1st. response from server is present
*   `socketOptions` **[Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)<[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)>** transparently passed to the WebSocket constructor

Returns **Store**&#x20;

# install

With [npm](http://npmjs.org) do:

```shell
npm install svelte-websocket-store
```

With [yarn](https://yarnpkg.com) do:

```shell
yarn add svelte-websocket-store
```

## run tests

```sh
export BROWSER=safari|chrome|...
npm|yarn test
```

# license

BSD-2-Clause
