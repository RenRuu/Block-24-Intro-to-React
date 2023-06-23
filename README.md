# Block-24-Intro-to-React

ReactJS is: 
    - Free and open source 
    - Front end JS library for building user interfaces
    - Based on 'components'
    - It is maintained by Meta (2011) and a community of individual developers and companies. 

JS library can be thought of as some pre-written js code which helps us solve difficult or time-consuming problems with ease. Also known as "Abstraction", it can provide a process of hiding away implementation and internal details, and presenting us only what we need. 
        'generalizing complex events in the real world to the concept'

    EX) UI > JS > C++ > Machine Language 

React is an 'abstraction' that helps us handle DOM update and forces us into a pattern.


React Component:
    Previously, content was separated in HTML, CSS, and JS (possible separate files) and renders them in the same place.
        - Rendering logic and markup live together in the same place = 'components'

    Ref: https://react.dev/learn/thinking-in-react

    Component is a piece of the UI that has its own logic and appearance. A component can be as small as a button, or as large as an entire page.

    "Class" based components is the old way of writing and is possible to still encounter called 'Legacy React'. This way is more complex with many 'lifecycle' methods to tap into React functionality. 

    Currently the standard is using "Hooks".


JSX:
    'JavaScript Syntax Extension'
    Looks like html but is stricter and can contain dynamic information.

    Note: JSX and React are two separate things. JSX is a syntax extension, while React is a JS library.


Nesting Components:
    - Can nest into other components 

    A component should ideally only do one thing. If it ends up growing it should be decomposed into smaller components.

Google search: "A nested component is any child component linked to a parent component. This relationship between the child and parent components is formed through composition rather than inheritance. This is to say that rather than inheriting one component from another, each component is created by assembling smaller ones."


Single Responsibility Principle
    Each component should only do one thing. ref: https://en.wikipedia.org/wiki/Single-responsibility_principle

    If the component grows, breaks it into sub components.

    Note: same way we nested elements within HTML, we can nest React components to build out our application. 


Listening for Events
    In vanilla DOM we need to add event listeners to a DOM reference from JS but in React we can simply add a listener DIRECTLY to the element. 

    Note: just like an even listener, we pass the onClick a function DEFINITION. Make sure not to 'INVOKE THE FUNCTION'. The onClick will be invoked when its respective element is clicked. 

    EX) function myButton () {
                return (
                    <button
                        onClick ={() => {
                        console.log("Clicked);
                        }}
                    >
                    Click Me!
                </button>
                );
            }


Hooks:
    What is Hooking?
        Any technique that is used to change or add to the behavior of an application by intercepting function calls, or event passed between components. 

        The code that handles these interceptions is called a 'Hook'. 

        Ref: https://react.dev/reference/react

        Hooks let you use different React features from your components.
            - Use the built in hooks or combine them to build you own.
            - Hooks can help us to synchronize external data and many other things.

    Most essential hook = useState

    useState:
        State let's a component 'remember' information about our component.

        EX) input form values, or a selected ID of an image in a gallery

        useState is a React Hook  that lets you add a 'state variable' to your component.

        Call 'useState' at the top level of your component to declare a 'state variable': 
            const [state, setState] = useState(initialState);

        The convention is to name state variables like [something, setSomething] using array destructuring. 
            const [state, setState] = useState(initialState);

        useState returns an array with exactly two Values:
            1. The current state. During the first render, it will match the 'initialState' you have passed.
            2. The 'set function' that lets you update the state to a different value and trigger a re-render.

                Note: Every time a state value updates = your components will re-render


"Escaping" into JS:
    To evaluate state variables or any JS, we can use curly brackets {} in React to "escape" into JS.

        EX) If we wanted to render a count variable made with use state to out browser, the component could look something like this:
            import React, { useState } from "react";
            
            export default function Counter () {
                const [cont,setCount] = useState {0};
                return <div>{count}</div>;
            }

        If the count state variable were to ever change, the evaluated JS inside the curly brackets would be re-evaluated.


Vite:
    A building tool that serves a local development server and bundles our application for production.

    It uses several tools 'under the hood' to bundle all of our JS files together, transpile our JS code, manage packages we may download through npm and more.
       - Means faster and more streamlined development 

    Ref = https://vitejs.dev/guide/

    




