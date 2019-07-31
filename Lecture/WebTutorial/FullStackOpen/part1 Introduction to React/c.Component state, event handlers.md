## Component state, event handlers
https://fullstackopen.com/en/part1/component_state_event_handlers
- Component helper functions
- Destructuring
- Page re-rendering
- Stateful component
  - https://reactjs.org/docs/hooks-state.html
- Event Handling
- Event handlers are functions
  - Too many re-renders issue.
    - Sol 1. array function
    - Sol 2. returns a function
- Function that returns a function
- Passing state to child components

#### 계속 루프 돌음
- Why? Button은 컴포넌트임;;

``` javascript
const Button = ({onClick, text}) => (
        <Button onClick={onClick}>{text}</Button>

)
```

- 그래서 아래처럼 button으로 수정

``` javascript
const Button = ({onClick, text}) => (
        <button onClick={onClick}>{text}</button>

)
```
