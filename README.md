# 30-DAYS-OF-FRONTEND
This repository contains 30 Topics on FRONT-END Technologies like HTML/CSS/REACT etc.

## Lists of Questions
1. [What is the difference between 'var', 'let' and 'const' keywords in Javascript?](#question-1)


## Question 1

  - The difference between these keywords can be simply categorized into 4 differnt topics, these are :
     1. Variable Hoisting
     2. Scope
     3. Top-level Binding
     4. Redeclaration Rules.
     
    ## Variable hoisting is done for variables declared with var and not with let
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

**[⬆ back to top](#lists-of-questions)**
