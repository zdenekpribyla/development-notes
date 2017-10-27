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