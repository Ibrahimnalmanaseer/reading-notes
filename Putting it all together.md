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

    we can identify the state need to live by determine the behave of our app .
    
    
### What is a “higher-order function”?

 a function can take one or more functions as an argument,  returning a function as the result


### Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

     to compare the function result with another function to return True if the second function than the first function .
     

### Explain how either map or reduce operates, with regards to higher-order functions.


