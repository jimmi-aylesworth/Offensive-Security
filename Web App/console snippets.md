Below snippets are handy for use within developer console. Unless otherwise noted, these apply to the current document.

Display links

```javascript
for (link of document.links ) {
   if(link.href.indexOf('example.com') == -1){
    console.log(link.href);
   }
}
```

Create an array of image links

```javascript
const pic_urls = [];
for(pic of document.images){
   pic_urls.push(pic.src);
}
console.log(pic_urls);
```

Get a list of all strings in code and print to console:

```javascript
for(prop in window) {
   if(typeof window[prop] === "string") {
      console.log(prop + ": " + window[prop]);
   }
}
```

Parse out the first chuck of a Java Web Token (JWT). Below assumes you have an item in local storage called "jwt".

```javascript
JSON.parse(atob(localStorage.getItem('jwt').split('.')[1]))
```
