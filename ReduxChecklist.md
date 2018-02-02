# Cheatsheet for Redux Hook Ups

    1. Create the reducer function
    2. Create a ./state folder in src
    3. Create store (store = createStore(reducer)
    4. Link it with your React app by using Provider
    
    const Root = () => {
        return (
            <Provider store={store}>
                <App />
            </Provider>
        );
    }
    ReactDOM.render(<Root />, document.getElementById('root'));
    
    5. "Wrap" each component that needs to get an update by…
        a. import {connect} from 'react-redux'
        b. Create two functions
            i. Map State to Props
            ii. Map Dispatch to Props
        c. 'connect' function takes those two functions and returns a function and pass that function
        the item that renders the object 
    
    const someName = connect(mapStateToProps, mapDispatchToProps)(Function That Renders an
