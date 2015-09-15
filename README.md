# Chainscript Client

## Example

### Creating a new script

```js
var Chainscript = require('chainscript-client').Chainscript;

// You pass the initial script
new Chainscript({document: 'My Document'})
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

### Starting from an existing script

```js
var Chainscript = require('chainscript-client').Chainscript;

Chainscript.load(
  // uuid of the existing script
  'chainscript:document:e1bdb650-1172-4d36-95c4-cef0f57c3a6f',
  function(err, script) {
    if (err) {
      console.log(err.message);
      return;
    }
    // You can add commands to the loaded script and run the script
    script
      .email('stephan.florquin+test@gmail.com')
      .run(function(err, script) {
        if (err) {
          console.log(err.message);
          return;
        }
        console.log(script.toJSON());
      });
  }
);
```
