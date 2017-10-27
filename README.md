# Development Notes

> Personal JavaScript codes


### Display only unique names of project

```javascript
var uniqueProjectNames = projectName.filter(function (item, index, record) {
    return record.indexOf(item) === index
});
console.log(uniqueProjectNames);
```