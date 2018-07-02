# is-support-passive-events

Determine if the current client support passive events.

``` javascript
function checkSupportPassiveEvents() {
  let passiveSupported = false;

  try {
    const options = Object.defineProperty({}, 'passive', {
      get() {
        passiveSupported = true;
      },
    });

    window.addEventListener('test', options, options);
    window.removeEventListener('test', options, options);
  } catch (err) {
    passiveSupported = false;
  }

  return passiveSupported;
}

export default checkSupportPassiveEvents();
```
