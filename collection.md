  
  
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
