# js 常用方法

- mergeObjects(obj1, obj2) - 合并对象方法

```typescript
function isObject(arg) {
  return arg != null && typeof arg === 'object' && !Array.isArray(arg)
}

function mergeObjects(obj1, obj2) {
  const result = Object.assign({}, obj1)
  if (isObject(obj1) && isObject(obj2)) {
    for (const p in obj2) {
      if (isObject(obj1[p]) && isObject(obj2[p])) {
        result[p] = mergeObjects(obj1[p], obj2[p])
      } else {
        result[p] = obj2[p]
      }
    }
  }
  return result
}
```

- isEmpty(obj) - 判断非空对象方法

```javascript
const isEmpty = (obj) =>
  Reflect.ownKeys(obj).length === 0 && obj.constructor === Object
```

- wait(milliseconds) - 延迟时间执行

```typescript
const wait = (milliseconds) =>
  new Promise((resolve) => setTimeout(resolve, milliseconds))
```
