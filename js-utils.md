# js常用工具集

#### 数组去重
```
var distinctArr = [...new Set(arr)]
```

### 深拷贝
```
function deepClone(target) {
  if (typeof target !== 'object' || target === null) {
    return target
  }
  
  let result
  if (Array.isArray(target)) {
    result = []
  } else {
    result = {}
  }
  for (const key in target) {
    if (Object.hasOwn(target, key)) {
      result[key] = deepClone(target[key])
    }
  }
  return result
}

```
