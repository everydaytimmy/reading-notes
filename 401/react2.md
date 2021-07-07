### React 2

#### Conditional Rendering:

https://reactjs.org/docs/conditional-rendering.html

##### Element Variables:
You can use variables to store elements. This can help you conditionally render a part of the component while the rest of the output doesn’t change.

##### Inline If with Logical && Operator:
You may embed expressions in JSX by wrapping them in curly braces. This includes the JavaScript logical && operator. It can be handy for conditionally including an element:

##### Inline If-Else with Conditional Operator:
Another method for conditionally rendering elements inline is to use the JavaScript conditional operator condition ? true : false.

##### Preventing Component from Rendering:
In rare cases you might want a component to hide itself even though it was rendered by another component. To do this return null instead of its render output.

#### Lists and Keys:

##### Rendering Multiple Components:
You can build collections of elements and include them in JSX using curly braces {}.

Below, we loop through the numbers array using the JavaScript map() function. We return a <li> element for each item. Finally, we assign the resulting array of elements to listItems:

```
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li>{number}</li>
```

```
ReactDOM.render(
  <ul>{listItems}</ul>,
  document.getElementById('root')
);
```

This code displays a bullet list of numbers between 1 and 5.

Keys
Keys help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity:

Extracting Components with Keys
Keys only make sense in the context of the surrounding array.

For example, if you extract a `ListItem` component, you should keep the key on the `<ListItem />` elements in the array rather than on the `<li>` element in the ListItem itself.



