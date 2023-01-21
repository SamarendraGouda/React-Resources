# [ReactJS] Calling a function in parent component from a child component

### Creating a function in Parent Component

###### Parent.js
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

###### Parent.js
``` 
  ...
  // Rendering the Child Component
  return(
    <Child handleClick={handleClick} />
  )
  
}
```

### Add the handleClick property to Child Component

###### Child.js
```
const Child = ({handleClick}) => {
...
}
```

### Calling the handleClick function from Child component

###### Child.js
```
...
return(
  <button onClick = {handleClick} > Click Here </button>
)
```
### Or calling the handleClick function inside another function

###### Child.js
```
...
const childFunction = () => {
  handleClick();
}

return (
  <button onClick={childFunction}> Click Here </button>
)
...
```

