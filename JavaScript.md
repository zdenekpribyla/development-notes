# JavaScript Notes

> The most popular JavaScript codes


### Display only unique names of project

```javascript
var uniqueProjectNames = projectName.filter(function (item, index, record) {
    return record.indexOf(item) === index
});
console.log(uniqueProjectNames);
```

### Merge values from group of arrays `AllTags` to one array
>source: https://stackoverflow.com/questions/5080028/what-is-the-most-efficient-way-to-concatenate-n-arrays-in-javascript
```javascript
var allTagsMerge = [].concat.apply([], allTags);
console.log(allTagsMerge);
```


### Display only array of `hours_spent` from `allData` 
```javascript
var allData = require('./file.json');
var allHoursArray = allData.map(function (record) {
    return record.hours_spent
});
console.log(allHoursArray);
```

### Sum values of `hours_spent` from `allHoursArray` by classic loop 

```javascript
var totalHours = 0;
for (i = 0; i < allHoursArray.length; i++) {
    totalHours += allHoursArray[i];
}
console.log(totalHours.toFixed(2));
```

### Sum values of `hours_spent` from `allHoursArray` by `loadash` functions
```javascript
var totalHours = _.sum(allHoursArray);
console.log(totalHours.toFixed(2));
```
### API download data from url - .json
```javascript
var url = 'https://api.github.com/users/zdenekpribyla/repos';
fetch(url)
    .then((resp) => resp.json())
.then(function(data) {
    }
}
```
### Create and add a new element into code (index.html)
>source:  // source: http://clubmate.fi/append-and-prepend-elements-with-pure-javascript/

```javascript
    jsonData.forEach(function (project) {
 // Where to put the new element   
     var parent = document.getElementById('result');
 // Make a new div
     var divChild = document.createElement("result__project");
 // Give the new div some content
     divChild.innerHTML = ('<h1>' + project.name + '</h1>');
 // Chug in into the parent element
     parent.appendChild(divChild);
     });
```

###If string contains defined text (eg. "http")
```javascript
if (url.indexOf("http") >= 0) {  //possible to use => url.include("http") === true
}
```

###typeOf return true/false depends of project type
```javascript
typeof 3 === "number"
true
typeof "text" === "string"
true
typeof "text" === "object"
false
```