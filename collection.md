  ### map
  
  ### forEach
  
  ### group
  group(collection, key)   
  group(collection, [predicate])   
    
  ```
  group(collection, predicate) {
    var realKey, isKey = typeof predicate === 'string'
    return collection.reduce((returnVal, item) => {
        realKey = isKey ? predicate : predicate(item);
        (returnVal[realKey] = returnVal[realKey] || []).push(item)
      return returnVal
    }, {})
  }
  ```
  
  ### findIndex
  ```
  var array = [{name: 'joe', age: 25}, {name: 'cora', age: 22}]
  array.findIndex(p => p.name==='joe')
  ```
