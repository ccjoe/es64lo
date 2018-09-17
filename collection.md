  group
  
  ```
  group(collection, key) {
    var realKey, isKey = typeof key === 'string'
    return collection.reduce((returnVal, item) => {
        realKey = isKey ? key : key(item);
        (returnVal[realKey] = returnVal[realKey] || []).push(item)
      return returnVal
    }, {})
  }
  ```
