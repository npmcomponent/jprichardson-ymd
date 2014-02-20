*This repository is a mirror of the [component](http://component.io) module [jprichardson/ymd](http://github.com/jprichardson/ymd). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/jprichardson-ymd`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
ymd
===

JavaScript component to return the year, month, and day string. i.e. returns `YYYY-MM-dd` from Date object.


Why?
----

It's a one liner that I got tired of writing over and over again.

Here it is:

```javascript
function ymd (date) {
  return date.getFullYear() + '-' + ('0' + (1 + date.getMonth())).slice(-2) + '-' + ('0' + date.getDate()).slice(-2)
}
```


Node.js/Browserify
------------------

    npm install --save ymd


Component
---------

    component install jprichardson/ymd


Methods
-------

### ymd

- returns using local timezone


### ymd.utc

- returns use UTC timezone


Example
------

```js
var ymd = require('ymd')

ymd.utc(new Date('2013-03-05')) //2013-03-05

// input to Date() is still being parsed as UTC, may be different for your timezone
ymd(new Date('2013-03-05 4:43 PM')) //2013-03-05
```


License
-------

(MIT License)

Copyright 2013, JP Richardson  <jprichardson@gmail.com>


