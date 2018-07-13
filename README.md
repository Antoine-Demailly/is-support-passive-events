# is-support-passive-events

Determine if the current client support passive events.

**New in v1.1.0 :** add `eventOptions()` to automatically fallback to basic options if passive events are not supported.

## Installation

```
npm install is-support-passive-events
```

## Usage example

``` javascript
import isSupportPassiveEvents from 'is-support-passive-events';
```

``` javascript
// When you're declaring your event, check if passive events are supported
const options = isSupportPassiveEvents
  ? { passive: true, capture: false }
  : false;
  
document.addEventListener('scroll', handler, options);
```

## `eventOptions(options [,fallback])` (function)

Automatically use a fallback if passive events are not supported.

Receives the following parameters :
- **options** (object)
- **fallback** (boolean) => Default value: `false`

``` javascript
import { eventOptions } from 'is-support-passive-events';
```

``` javascript
document.addEventListener('scroll', handler, eventOptions({
  passive: true, capture: false
}));
```

