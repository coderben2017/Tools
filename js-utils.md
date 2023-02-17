# js常用工具集

#### 数组去重
```
var distinctArr = [...new Set(arr)]
```

### 深拷贝
```
function deepClone(target, result = new WeakMap()) {
  if (typeof target !== 'object' || target === null) {
    return target
  }
  
  if (result.has(target)) {
    return result.get(target)
  }

  if (target.constructor === Function) {
    return new Function(`return ${target.toString()}`)()
  }
  
  if (target.constructor === RegExp || target.constructor === Date) {
    return new target.constructor(target)
  }

  if (target instanceof Proxy) {
    return target
  }

  if (target instanceof Set) {
    const newSet = new Set()
    target.forEach(value => {
      newSet.add(deepClone(value, result))
    })
    result.set(target, newSet)
    return newSet
  }

  if (target instanceof Map) {
    const newMap = new Map()
    target.forEach((value, key) => {
      newMap.set(key, deepClone(value, result))
    })
    result.set(target, newMap)
    return newMap
  }

  const newObj = Array.isArray(target) ? [] : {}
  result.set(target, newObj)

  for (let key in target) {
    newObj[key] = deepClone(target[key], result)
  }

  return newObj
}
```
