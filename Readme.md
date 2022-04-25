This library is to be used in conjunction with https://github.com/dolanmiu/docx

It extracts paragraph types and text styles for use with docx.

Types of paragraph:
```
<p>: 'paragraph'
<blockquote>: 'quote'
<li>: bullet

Styles:
<b>
<em>
<a>
```
all other html tags are removed from the text.

```
const { htmlToDocxObject } = require('html-to-docx')

htmlToDocxObject(string)
```
returns an array of objects, one object for each paragraph:
```
[{
    sections: [{ 
        text: <string>, 
        bold: <bool>, 
        italics: <bool>, 
        link: <null/string> 
    }],
    paragraphType: <string>
}]
```
