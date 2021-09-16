
# useEffect

useEffect ( ( ) => { }, [ ] );

## Things to learn about useEffect hook

01. This hook runs a function on every render of the component but we can control it
02. It runs the function initially when the component first renders
03. It also runs the function when the state changes. That's because the componet re-renders due to data/state change
04. This hook is a way to run code on every render 
05. We can use this hook for fetching data, communicate with authentication services etc. These are called 'side effects' in React

## useEffect dependencies
01. If we don't want to run the function inside useEffect( ) on 'every render', we can set dependencies
02. We can set dependencies by putting an array [ ] as the second parameter of the useEffect hook
03. If the array [ ] is empty, useEffect runs the function inside it once on the initial render and not after state/data change
04. But if we want to run the function on certain condition(s) like any data/state change, we can set the data/state as the item(s) of the dependency array like useEffect ( ( ) => { }, [state, data] )

## Useful resources for learning useEffect

01. This link can be very useful for learning useEffect:  https://dmitripavlutin.com/react-useeffect-explanation/
02. React's own document on useEffect:  https://reactjs.org/docs/hooks-effect.html


# useRef

const refContainer = useRef ( initialValue ); 

## Things to learn about useRef hook
01. useRef(initialValue) accepts one argument as the initial value and returns a reference (aka ref). A reference is an object having a special property "current".
02. There are 2 rules to remember about references: <b>(i)</b> The value of the reference is persisted (stays the same) between component re-renderings; <b>(ii)</b> Updating a reference doesn’t trigger a component re-rendering.

## The 2 main differences between reference and state 
01. Updating a reference doesn’t trigger re-rendering, while updating the state makes the component re-render;
02. The reference update is synchronous (the updated reference value is available right away), while the state update is asynchronous (the state variable is updated after re-rendering).

## Other info
From a higher point of view, references store infrastructure data of side-effects, while the state stores information that is directly rendered on the screen.

You can store inside a reference infrastructure data of side effects. For example, you can store into reference pointers: timer ids, socket ids, etc.

## Accessing DOM elements 
Another useful application of the useRef() hook is to access DOM elements. This is performed in 3 steps:

1. Define the reference to access the element: const elementRef = useRef();
2. Assign the reference to ref attribute of the element: &lt;div ref={elementRef}&gt;&lt;/div&gt;;
3. After mounting, elementRef.current points to the DOM element

## Ref is null on initial rendering
During initial rendering React still determines what is the output of the component, so there’s no DOM structure created yet. That’s why inputRef.current evaluates to undefined during initial rendering.