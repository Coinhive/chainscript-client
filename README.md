# Chainscript Client

## Example

```js
var Chainscript = require('chainscript-client').Chainscript;

// You pass the initial document
var script = new Chainscript('My Document');

script.run(function(err) {
  if (err) {
    console.log(err.message);
    return;
  }
  console.log(script.toJSON());
});

```
