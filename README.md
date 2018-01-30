# Redux_Flux

npm install --save Redux React-Redux (to bring packages in)

reducers take state and an action

function reducer(state, action)

the action.type is always a string

the reducer returns state items

```
const TITLE_UPDATE = `alsdkjlaskdfj`
const CONTENT_UPDATE = `laskjdflaskjf1


let initialState = {
  title: 'Hi There',
  content: []
}

let currentState = initialState;

function reducer(state=initialState, action) {  // setting state = initialstate will use the initialState if an 'undefined' parameter is passed
  swtich(action.type) {
    case TITLE_UPDATE:
      return { ...state, title: action.data};
    case CONTENT_UPDATE:
      return { ...state, content: state.content.concat([action.payload])};
    default:
      return state;
  }
}


to test
console.log(reducer(initialState, {type: TITLE_UPDATE, payload: `new stuff for the title`}));
console.log(reducer(initialState, {type: CONTENT_UPDATE, payload: `new stuff for the title`}));

function render(state){
  titleValue.innerText = state.title;
  state.content.forEach(content => {
  let str = '';
  state.content.forEach(() => {
  str += content + '/n'
  }
  });
}

render(initialState);

submitContent.addEventListener('click', () => {
  const value = input.value;
  currentState = reducer(currentState, {type: CONTENT_UPDATE, payload: value})
  render(currentState)
})

submitTitle.addEventListener('click', () => {
  const value = input.value;
  currentState = reducer(currentState, {type: TITLE_UPDATE, payload: value})
  render(currentState)
})
```
