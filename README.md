# React-Quickstart-Guide
Explore the fundamentals of React with clear and concise examples. From creating components to handling state and events, this repository serves as a beginner-friendly guide to kickstart your React journey.

In React apps, understanding the following concepts is essential:

## Building Components:
In React, a component can only return a single element. To return multiple elements, we use a fragment represented by empty angle brackets.

```
const Message = () => {
  return (
    <>
      <h1>Hello world</h1>
      <p>Hello</p>
    </>
  );
};

export default Message;

```
## Immutable Props:
It's crucial to treat props (short for properties) as immutable (read-only) and not modify them.

```
interface Props {
  name: string;
}

const Component = ({ name }: Props) => {
  return <p>{name}</p>;
}

```
## State Hook:
The state hook **(useState)** is used to define state (data that can change over time) in a component. It allows us to tap into built-in features in React.
```
const [isOpen, setIsOpen] = useState(false);
```
## Rendering a List:
To render a list in JSX, we use the **array.map()** method. Each item must have a unique key, which can be a string or a number.
```
const Component = () => {
  const items = ["a", "b", "c", "d"];
  return (
    <ul>
      {items.map((item) => (
        <li key={item}>{item}</li>
      ))}
    </ul>
  );
};

```
## Conditional Rendering:
We can conditionally render content using an 'if' statement or a ternary operator.
```
{items.length === 0 ? <p>No item found</p> : null}
{items.length === 0 && <p>No item found</p>}

```
## Handling Events:
Events like onClick can be handled in React components to respond to user interactions.
```
<button onClick={() => console.log('clicked')}></button>

```
## Passing Children:
Components can receive and render children components using the children prop.
```
interface Props {
  children: ReactNode;
}

const Component = ({ children }: Props) => {
  return <p>{children}</p>;
};

```
