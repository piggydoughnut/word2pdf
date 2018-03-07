# About

Original package can be found at https://github.com/VuongVu/word2pdf

I created this fork because I ran into issues when using this package for AWS Lambda, which does not support the newest node version (async/await).

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

```javascript
const word2pdf = require('word2pdf-promises');
const fs = require('fs');
```

Using file path

```javascript
const convert = () => {
	word2pdf.word2pdf('test.docx')
		.then(data => {
			fs.writeFileSync('test.pdf', data);
		})
}
```

Using Buffer

```javascript
const convert = () => {
	word2pdf.word2pdfBuffer(bufferObject)
		.then(data => {
			fs.writeFileSync('test.pdf', data);
		})
}
```
