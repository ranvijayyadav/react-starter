# react-starter
Starter kit for react with best practices


#Basics
 React.Component subclass
```
 class ShoppingList extends React.Component {
  render() {
    return (
      <div className="shopping-list">
        <h1>Shopping List for {this.props.name}</h1>
        <ul>
          <li>Instagram</li>
          <li>WhatsApp</li>
          <li>Oculus</li>
        </ul>
      </div>
    );
  }
}
```

this is equivalent to
```
return React.createElement('div', {className: 'shopping-list'},
  React.createElement('h1', /* ... h1 children ... */),
  React.createElement('ul', /* ... ul children ... */[
      React.createElement('li', /* ... li children ... */),
      React.createElement('li', /* ... li children ... */),
      React.createElement('li', /* ... li children ... */)])
);
```

Syntax of createElement() is as follows

```
React.createElement(
  type,
  [props],
  [...children]
)
```

Create and return a new React element of the given type. The type argument can be either a tag name string (such as 'div' or 'span'), a React component type (a class or a function), or a React fragment type.

Code written with JSX will be converted to use React.createElement(). You will not typically invoke React.createElement() directly if you are using JSX.

createElement takes three parmeters "type", "props", children
    1. type : type defines the type of reactelement 
    2. props : props are list of properties passed to the react component
    3. children : A react component can be composed of multiple compoenent those constituent component are called as children







