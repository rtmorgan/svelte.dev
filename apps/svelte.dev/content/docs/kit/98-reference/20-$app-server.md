---
title: $app/server
---



```js
// @noErrors
import { read, websocket } from '$app/server';
```

## read

Read the contents of an imported asset from the filesystem

```js
// @errors: 7031
import { read } from '$app/server';
import somefile from './somefile.txt';

const asset = read(somefile);
const text = await asset.text();
```

<div class="ts-block">

```dts
function read(asset: string): Response;
```

</div>



## websocket

Check if WebSocket connections are supported in the current environment

```js
// @errors: 7031
import { websocket } from '$app/server';

const isSupported = websocket();
```

<div class="ts-block">

```dts
function websocket(): boolean;
```

</div>




