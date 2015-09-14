# Chainscript Client

## Example

```js
var Chainscript = require('chainscript-client').Chainscript;

// You pass the initial document
new Chainscript('My Document')
  // Add a snapshot command
  .snapshot()
  // Add a send mail command
  .email('stephan.florquin+test@gmail.com')
  // Run the script
  .run(function(err, script) {
    if (err) {
      console.log(err.message);
      return;
    }
    console.log(script.toJSON());
  });
```
