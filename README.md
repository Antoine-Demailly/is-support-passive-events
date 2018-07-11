# is-support-passive-events

Determine if the current client support passive events.

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
