# Development Notes

> Personal JavaScript codes


### Display only unique names of project

```javascript
var uniqueProjectNames = projectName.filter(function (item, index, record) {
    return record.indexOf(item) === index
});
console.log(uniqueProjectNames);
```

### Merge values from group of arrays `AllTags` to one array

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
```
var totalHours = _.sum(allHoursArray);
console.log(totalHours.toFixed(2));
```