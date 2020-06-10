# 30-DAYS-OF-FRONTEND
This repository contains 30 Topics on FRONT-END Technologies like HTML/CSS/REACT etc.

## Lists of Questions
1. [What is the difference between 'var', 'let' and 'const' keywords in Javascript?](#answer-1)


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
