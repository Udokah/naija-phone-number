[![npm version](https://badge.fury.io/js/naija-phone-number.svg)](https://badge.fury.io/js/naija-phone-number) [![Build Status](https://travis-ci.org/Udokah/naija-phone-number.svg?branch=master)](https://travis-ci.org/Udokah/naija-phone-number)

## Naija Phone Number
A fast minimal library to validate a Nigerian phone number using Regular Expressions.

### Installation
```
$ npm install naija-phone-number --save
```

### Usage

This library assumes that you already know that Nigerian numbers
are prefixed by `+234` and you should not expect your users to type that. Instead your UI should look something like this.

``` 
     |**********************|
+234 |  phone number here   |
     |**********************|
```

Now that we've gotten this out of the way here's an example

```js
const naijaNumber = require('naija-phone-number');

// 11 digit numbers
naijaNumber.isValid('09052858232'); // true

// 12 digit numbers
naijaNumber.isValid('070328582392'); // true

// Pass argument as Number
naijaNumber.isValid(081928582392); // true

naijaNumber.isValid(081028582392); // true

naijaNumber.isValid(050728582392); // false
```
