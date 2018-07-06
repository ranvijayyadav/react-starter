
#Basics

React is devided in two basic parts

    1. React core(create element, lifecycle method)
    2. Render engine specific lib(react-dom, react-native, react-vr etc)

#React core

This is core library of react which handles things like `createlement` and `lifecycle method`

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

Create and return a new React element of the given type. The type argument can be either a tag name string (such as 'div' or 'span'), a React component type (a class or a function), or a React [fragment type](https://reactjs.org/docs/fragments.html).

Code written with JSX will be converted to use React.createElement(). You will not typically invoke React.createElement() directly if you are using JSX.

createElement takes three parmeters "type", "props", children
    1. type : type defines the type of reactelement 
    2. props : props are list of properties passed to the react component
    3. children : A react component can be composed of multiple compoenent those constituent component are called as children

React core also provide react [lifecycle method](https://reactjs.org/docs/state-and-lifecycle.html#adding-lifecycle-methods-to-a-class) 




React Render 

Using core react library we can create component but to display these component into differnt type of system(web, vr etc) React provides a glue layer which enables these coomponent to render
we have many render lib for web (react-dom), native(react native), VR(react vr) etc

#React-dom

