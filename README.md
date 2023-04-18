# web-quoted-printable-decoder

A quoted printable decoder that can be used on the web

Every quoted printable decoder that I found on the internet was base on Nodejs, so I decided to make one that doesn't require any extra-dependency or Nodejs functions, making it run in the browser.

The code was heavily borrowed from [andris9's libmime](https://github.com/nodemailer/libmime), I just adapted stuff, removing depencencies from other libraries and from Node modules so it can run in the browser

## Usage

**With NPM:**

Install the package with:

`npm i web-quoted-printable-decoder`

And then:

```js
const decoder = require('web-quoted-printable-decoder');

const originalString = "=?UTF-8?q?Att._Hugo_-_Convite_Israel_360°?";

var decodedString = decoder.decodeQuotedPrintable();

console.log(decodedString);
//prints: Att. Hugo - Convite Israel 360°
```

**In your browser:**

Import the script with:

`<script src="https://cdn.kunum.com/wqpd.js"></script>`

And then:

```js
console.log(decodeQuotedPrintable("=?UTF-8?q?Att._Hugo_-_Convite_Israel_360°?"));
//prints: Att. Hugo - Convite Israel 360°
```

## Notes

Please notice that this package only decodes **quoted printable** and **base64** encodings.

Feel free to contribute ;)
