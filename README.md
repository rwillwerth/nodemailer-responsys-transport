# Nodemailer-Responsys-Transport

Send transactional style emails through the Responsys API.

### Example

```js
'use strict';

var nodemailer = require('nodemailer');
var responsysTransport = require('nodemailer-responsys-transport');

var transport = nodemailer.createTransport(responsysTransport({
  auth: {
    username: 'username',
    password: 'password'
  },
  campaignName: 'Rebelmail'
}));

transport.sendMail({
  to: 'user@example.com',
  html: '<p>How are you?</p>'
}, function(err, info) {
  console.log(arguments);
});
```
