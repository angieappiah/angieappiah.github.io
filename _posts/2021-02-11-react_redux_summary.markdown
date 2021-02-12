---
layout: post
title:      "REACT/REDUX Summary"
date:       2021-02-12 02:00:13 +0000
permalink:  react_redux_summary
---


In planning my react/redux portfolio project, I wanted a clear picture of how the different parts of the App would work together. I decided to read about the major features that would be beneficial to the development of the App. Below are some of these features and how they function. 

**Redux Store** 
The redux store is a container that holds your application's state.

**Actions and Action creators**
Actions are plain JavaScript objects that have a type field that describe what happens in the application. Action Creators, on the other hand are the functions that create the actions.

**Reducers**
They are functions that take the current state and an action as argument and return a new state. It accepts the previous state of app and action being dispatched and returns the new object. Reducers cannot modify the existing states.

**DevTools**
These are tools that help developers track everything going on in the app, from actions to state changes. It offers debugging features which include allowing developers to inspect every state and action payload, helping developers navigate the exact location in a code, and also enabling developers to quickly move around and see the app’s output on different states.

**Routing**
Routing means using a path to direct different parts in an application by keeping the browser URL in sync with what’s being rendered on the page. Routing in React can be achieved through a React-Router library. React-Router gives access to a number of routers including BrowserRouter, which is used for dynamic server applications. 

In learning about these different features and using them to develop my app, I have gained a deeper understanding into how the features communicate with each other in building the App.


