# Thinking in React

### What is the single responsibility principle and how does it apply to components?

    is atechinque component should ideally only do one thing
  

### What does it mean to build a ‘static’ version of your application?

   not an interactivly app which rendering a data model by build components that reuse other components and pass data using props.

### Once you have a static application, what do you need to add?
    build component and pass data by props .
    
### What are the three questions you can ask to determine if something is state?

      Is it passed in from a parent via props? If so, it probably isn’t state.
      Does it remain unchanged over time? If so, it probably isn’t state.
      Can you compute it based on any other state or props in your component? If so, it isn’t state.
      
### How can you identify where state needs to live?

