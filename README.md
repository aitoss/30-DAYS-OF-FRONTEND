# 30-DAYS-OF-FRONTEND
This repository contains 30 Topics on FRONT-END Technologies like HTML/CSS/REACT etc.

## Lists of Questions
1. [What is the difference between 'var', 'let' and 'const' keywords in Javascript?](#answer-1)
2. [What is the best way to include a Javascript file in a HTMl document? - like where should we include it, how we include  it and why?](#answer-2)
3. [What is the difference between a Library and a Framework? It would be great if you list some examples too.](#answer-3)
4. [What is Specificity in CSS and why is it important?](#answer-4)
5. [What is Event Bubbling and Event Capturing in Javascript?](#answer-5)
6. [How do we handle asynchronous functionality in javascript? (Read about - Callbacks, Promises, Async Await and understand their differences.)](#answer-6)
7. [What is Lazy Loading and why should we use it ? (with some example use cases)](#answer-7)
8. [(React#1): Why react over traditional web development?](#answer-8)
9. [What is Browser Storage? Understand/List down some of its use cases. (Explore - cookies  , web storage [ local storage, session storage] and understand the differences)](#answer-9)
10. [(React#2): What is state and what are props in react? Understand them thoroughly as they are the most important part of react. Understand which should be used when and then identify the difference between functional components and class components.](#answer-10)
11. [What is the "this" keyword and how does it work?](#answer-11)
12. [(React#3): What is setState, why do we use setState to change the value of state instead of just asssigning a new value and how does it works?](#answer-12)
13. [What do you understand by Explicit Binding? Understand the use and differences(good and bad parts) between .call, .bind, .apply (For those learning react, try to figure out how bind is used at places)](#answer-13)
14. [(React#4): What do you understand by 'lifecycle of a component' in react? Undertstand different lifecycle methods and their use cases.](#answer-14)
15. [What are the different CSS positions? Understand them properly, figure out their use cases and compare them.](#answer-15)
16. [Is Javascript Object-Oriented? State reasons for your answer.](#answer-16)
17. [What do you understand by programming paradigm? Explore its types and then try to understand which programming paradigm does Javascript follows!](#answer-17)
18. [(React#5): What are Keys in react and why are they important?](#answer-18)
19. [(React#6): Explain about events in react and how do we handle/use them.](#answer-19)
20. [What are flexbox? Explore and understand (by writing sample codes) its various usage.](#answer-20)
21. [ What are .map(), .filter() and .reduce? Understand their usage, difference and also try out sample code for each one of them.](#answer-21)
22. [What is DOM? Explain your understanding of it and state some good usage/facts/features around it.](#answer-22)
23. [What is the significance, and what are the benefits, of including 'use strict' at the beginning of a JavaScript source file?](#answer-23)
24. [What are closures? Explain its importance and use.](#answer-24)


## Answer 1

  - The difference between these keywords can be simply categorized into 4 differnt topics, these are :
     1. Variable Hoisting
     2. Scope
     3. Top-level Binding
     4. Redeclaration Rules.
     
  ## a.) Variable hoisting is done for variables declared with var and not with let
   ### Ques:  What does hoisting mean?
   Ans: Hoisting is a mechanism in javascript where all the variables declared with var and declared functions are                   moved to the top of their scope before the actual execution of the code starts. In case you wondered why you                 were able to call functions before the declaration. This was the reason.
        So, for var what happens is you can use the variable before the declaration and the engine will not throw an                 error while executing the code.
           
   **Example Code (var):**
   
   ```javascript
        console.log(a);
        var a=10;
        console.log(a);
   ```
   **After Hoisting:**
   
   ```javascript
        var a;
        console.log(a);
        a=10;
        console.log(a);
   ```
   **Result**
    
   ```javascript
        undefined
        10
   ```
   **Example Code (let):**
  
   ```javascript
        console.log(a);
        let a=10;
   ```
   **After Hoisting:**
   
   ```javascript
        console.log(a);
        let a=10;
   ```
   **Result**
   
   ```javascript
        Line 1: ReferenceError: Cannot access 'a' before initialization
   ```
    
  ## b.) var is scoped to the immediate outer function.
  var is scoped to the immediate outer function of where the var declaration is done, while let is block scoped.
  
   **Example Code (let):**

  ```javascript
      for(let i=0;i<10;i++) {
      console.log(i); //i is visible thus is logged in the console as 0,1,2,….,9
       }
      console.log(i); //throws an error as “i is not defined” because i is not visible
  ```
   **Example Code (var):**

  ```javascript
       for(var i=0; i<10; i++) {
       console.log(i); //i is visible thus is logged in the console as 0,1,2,….,9
       }
       console.log(i); //i is visible here too. thus is logged as 10.
  ```

 ## c.) var on top-level binds to the global object.
  Var on the top-level binds to the global object (window object) while let doesn’t.
  
   **Example :**

  ```javascript
      var x = ‘global’;
      let y = ‘global’;
      console.log(this.x); // “global”
      console.log(this.y); // undefined
  ```

## d.) Redeclaration
  In the case of var, redeclaration is possible while in the case of let redeclaration is not possible.
  
   **Example Code:**

  ```javascript
     var foo = “foo1”;
     var foo = “foo2”; // No problem, ‘foo’ is replaced.
     let bar = “bar1”;
     let bar = “bar2”; // SyntaxError: Identifier ‘bar’ has already been declared
  ```
    
**[⬆ back to top](#lists-of-questions)**


## Contributors
* Sudhanshu Joshi - [SJoshi7](https://github.com/SJoshi7)
* Akshay Sharma - [AkshaySharma008](https://github.com/AkshaySharma008)
