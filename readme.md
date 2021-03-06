

# pwmetrics

> Progressive web metrics at your fingertipz. 💅

CLI tool and lib to gather performance metrics via [Lighthouse](https://github.com/GoogleChrome/lighthouse/). _IN BETA_.

![image](https://cloud.githubusercontent.com/assets/39191/17918763/a18b78f0-697c-11e6-939f-2fb3b3fad8d9.png)

 Documentation on these metrics in the works. If you hit bugs in the metrics collection, report at [Lighthouse issues](https://github.com/GoogleChrome/lighthouse/issues).

### Install [![NPM pwmetrics package](https://img.shields.io/npm/v/pwmetrics.svg)](https://npmjs.org/package/pwmetrics)
```sh
$ npm install --global pwmetrics
# or
$ npm install --save pwmetrics
```


### CLI Usage

```sh
# run Chrome with port 9222 open
chrome  --remote-debugging-port=9222 --no-first-run --user-data-dir=$(mktemp -d -t pwm.XXXXX)

# run pwmetrics with your url
pwmetrics http://goat.com
```

#### Options

```sh
# --json
pwmetrics --json http://example.com

# returns...
# {
#   "timings": [
#     {
#       "name": "First Contentful Paint",
#       "value": 289.642
#     },
#     {
#       "name": "First Meaningful Paint",
#       "value": 289.6
#     },
#     ...
```

### API

```js
const PWMetrics = require('pwmetrics');


new PWMetrics('http://bubbles.com', opts);
```


### License

Apache 2.0. Google Inc.
