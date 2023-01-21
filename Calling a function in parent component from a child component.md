# [ReactJS] Calling a function in parent component from a child component

### Creating a function in Parent Component

```
import Child from "./../Components/Child/Child.js"

const Parent = () => {
  
  // Creating a function in Parent Component
  const handleClick = () => {
    console.log("Parent Function Called")
  }
  ...
```
### Rendering the Child Component from parent component
``` 
  ...
  // Rendering the Child Component
  return(
    <Child handleClick={handleClick} />
  )
  
}
```

### Add the handleClick property to Child Component

```
const Child = ({handleClick}) => {
...
}
```

### Calling the handleClick function from Child component

```
...
return(
  <button onClick = {handleClick} />
)
```

