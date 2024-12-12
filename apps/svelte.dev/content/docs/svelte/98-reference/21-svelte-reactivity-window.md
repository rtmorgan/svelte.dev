---
title: svelte/reactivity/window
---

This module exports reactive versions of various `window` values, each of which has a reactive `current` property that you can reference in reactive contexts (templates, [deriveds]($derived) and [effects]($effect)) without using [`<svelte:window>`](svelte-window) bindings or manually creating your own event listeners.

```svelte
<script>
	import { innerWidth, innerHeight } from 'svelte/reactivity/window';
</script>

<p>{innerWidth.current}x{innerHeight.current}</p>
```



```js
// @noErrors
import {
	devicePixelRatio,
	innerHeight,
	innerWidth,
	online,
	outerHeight,
	outerWidth,
	screenLeft,
	screenTop,
	scrollX,
	scrollY
} from 'svelte/reactivity/window';
```

## devicePixelRatio

`devicePixelRatio.current` is a reactive view of `window.devicePixelRatio`. On the server it is `undefined`.
Note that behaviour differs between browsers — on Chrome it will respond to the current zoom level,
on Firefox and Safari it won't.

<div class="ts-block">

```dts
const devicePixelRatio: {
	get current(): number | undefined;
};
```

</div>



## innerHeight

`innerHeight.current` is a reactive view of `window.innerHeight`. On the server it is `undefined`.

<div class="ts-block">

```dts
const innerHeight: ReactiveValue<number | undefined>;
```

</div>



## innerWidth

`innerWidth.current` is a reactive view of `window.innerWidth`. On the server it is `undefined`.

<div class="ts-block">

```dts
const innerWidth: ReactiveValue<number | undefined>;
```

</div>



## online

`online.current` is a reactive view of `navigator.onLine`. On the server it is `undefined`.

<div class="ts-block">

```dts
const online: ReactiveValue<boolean | undefined>;
```

</div>



## outerHeight

`outerHeight.current` is a reactive view of `window.outerHeight`. On the server it is `undefined`.

<div class="ts-block">

```dts
const outerHeight: ReactiveValue<number | undefined>;
```

</div>



## outerWidth

`outerWidth.current` is a reactive view of `window.outerWidth`. On the server it is `undefined`.

<div class="ts-block">

```dts
const outerWidth: ReactiveValue<number | undefined>;
```

</div>



## screenLeft

`screenLeft.current` is a reactive view of `window.screenLeft`. It is updated inside a `requestAnimationFrame` callback. On the server it is `undefined`.

<div class="ts-block">

```dts
const screenLeft: ReactiveValue<number | undefined>;
```

</div>



## screenTop

`screenTop.current` is a reactive view of `window.screenTop`. It is updated inside a `requestAnimationFrame` callback. On the server it is `undefined`.

<div class="ts-block">

```dts
const screenTop: ReactiveValue<number | undefined>;
```

</div>



## scrollX

`scrollX.current` is a reactive view of `window.scrollX`. On the server it is `undefined`.

<div class="ts-block">

```dts
const scrollX: ReactiveValue<number | undefined>;
```

</div>



## scrollY

`scrollY.current` is a reactive view of `window.scrollY`. On the server it is `undefined`.

<div class="ts-block">

```dts
const scrollY: ReactiveValue<number | undefined>;
```

</div>




