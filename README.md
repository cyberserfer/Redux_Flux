# Redux_Flux

reducers take state and an action

function reducer(state, action)

the action.type is always a string

the reducer returns state items

```
const TITLE_UPDATE = `alsdkjlaskdfj`
const CONTENT_UPDATE = `laskjdflaskjf1

let state = {
  title: '',
  content: []
}

function reducer(state, action) {
  swtich(action.type) {
    case TITLE_UPDATE:
      return { ...state, title: action.data};
    case CONTENT_UPDATE:
      return { ...state, content: state.content.concat([action.payload])};
    default:
      return state;
  }
}
