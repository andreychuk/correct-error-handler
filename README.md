[![Build Status](https://travis-ci.org/kozzztya/correct-error-handler.svg?branch=master)](https://travis-ci.org/kozzztya/feathers-validation)

# correct-error-handler

Just correct implementation of error handler for Express.JS and FeathersJS apps.
Set ROLLBAR_TOKEN env var to send errors to Rollbar.

## Usage

For FeathersJS apps:

```js
const errorHandler = require("correct-error-handler");

// some middlewares

app.configure(errorHandler);
```

For Express.JS apps:

```js
const errorHandler = require("correct-error-handler");

// some middlewares

errorHandler(app);
```

Or:

```js
const errorHandler = require("correct-error-handler/basic");
const rollbar = require("correct-error-handler/rollbar");

// some middlewares

app.use(rollbar());
app.use(errorHandler());
```
