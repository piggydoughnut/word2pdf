# About

Original package can be found at https://github.com/VuongVu/word2pdf

I created this fork because I ran into issues when using this package for AWS Lambda, which does not support the newest node version (async/await).

It is exactly the same, just replaces async/await with promises.

# Install package

Run cmd with
```sh
npm i word2pdf-promises
```
 or
 ```sh
 yarn add word2pdf-promises
 ```

# Uses

Example

```javascript
const word2pdf = require('word2pdf-promises');
const fs = require('fs');

const convert = () => {
	word2pdf('test.docx')
		.then(data => {
			fs.writeFileSync('test.pdf', data);
		})
}
```
