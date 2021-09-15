
# useEffect

useEffect ( () => { }, [ ] );

## Things to learn about useEffect hook:

01. This hook runs a function on every render of the component but we can control it
02. It runs the function initially when the component first renders
03. It also runs the function when the state changes. That's because the componet re-renders due to state/data change
04. This hook is a way to run code on every render 
05. We can use this hook for fetching data, communicate with authentication services etc. These are called 'side effects' in React

## useEffect dependencies
01. If we don't want to run the function inside useEffect() on 'every render', we can set dependencies
02. We can set dependencies by putting an array [] as the second parameter of the useEffect hook
03. If the array [] is empty, useEffect runs the function inside it once on the initial render and not after state/data change
04. But if we want to run the function on certain condition(s) like any data/state change, we can set the data/state as the item(s) of the dependency array like useEffect ( () => { }, [state, data] )

## Useful sources

01. This link can be very useful for learning useEffect:  https://dmitripavlutin.com/react-useeffect-explanation/
02. React's own document on useEffect:  https://reactjs.org/docs/hooks-effect.html
