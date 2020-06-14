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
    
**[⬆  back to top](#lists-of-questions)**

## Answer 2
  ### About JavaScript
  JavaScript, also abbreviated to JS, is a programming language used inweb development and nowadays in ML too. As one of the  core technologiesof the web alongside HTML and CSS, JavaScript is used to make webpagesinteractive and to build web apps.
  
  ### Features :
  •JavaScript   is   a   scripting   language   and   lightweight   programminglanguage 
  •JavaScript is usually embedded directly into HTML pages 
  •JavaScript is an interpreted language (means that scripts executewithout preliminary compilation)
  •JavaScript can add interactivity to HTML pages
  
  ### Advantages:
  #### Minimalized   server   interaction:
  if   you   want   to   optimize   theperformance of a website, the best way is to reduce the communicationwith the server. JavaScript helps in this regard by validating userinput at the client-side. It only sends requests to the server afterrunning the initial validation checks.
  #### Richer, user-friendly interfaces
  #### Immediate Feedback to the User
  #### Easy debugging:
  JavaScript is an interpreted language, which meansthat written code gets deciphered line by line. In case any errors popup, you will get the exact line number where the problem lies.
  
 ## Syntax and option to include JS in HTML file:
 You can include JavaScript in your HTML in two ways:
   ### 1. Writing the code in your HTML 
   #### Syntax:
   ```
   <script>document.getElementById("demo").innerHTML   =   "My   First   JavaScript";</script>
   ```
   coding JS inside same HTML file is preferred very less in good codingpractice.so , we prefer mostly external scripting.
   
   ### 2. Including it as a link to an external file 
   #### Syntax:
   ```
   <script src="myScript.js"></script>
   ```
   External   scripts   are   practical   when   the   same   code   is   used   in   manydifferent   web   pages.   Placing    scripts   in   external   files   has   someadvantages:
   •It separates HTML and code 
   •It makes HTML and JavaScript easier to read and maintain 
   •Cached JavaScript files can speed up page loadsScripts can be placed in the <body>, or in the <head> section of anHTML page, or in both.
  
  It was a <b> best practice</b> in older times to put JavaScript <script> tagsjust before the closing </body> tag rather   than in the <head> section ofyour HTML.The reason for this is that HTML loads from top to bottom. The headloads first, then the body, and then everything inside the body. If weput our JavaScript links in the head section, the entire JavaScript file will   load   before   loading   any   of   the   HTML,   which   could   cause   a   few problems.
  1.If you have code in your JavaScript that alters HTML as soon as theJavaScript file loads, there won't actually be any HTML elementsavailable for it to affect yet, so it will seem as though theJavaScript code isn't working, and you may get errors. 
  2.If you have a lot of JavaScript, it can visibly slow the loading ofyour page because it loads all of the JavaScript before it loadsany of the HTML. 
  When you place your JavaScript links at the bottom of your HTML body, itgives the HTML time to load before any of the JavaScript loads, whichcan prevent errors, and speed up website response time.
  This approach has its own problem:
  The   browser   cannot   start   downloading   the   scripts   until   the   entiredocument   is   parsed.   For   larger   websites   with   large   scripts   &stylesheets, being able to download the script as soon as possible isvery important for performance. If your website doesn't load within 2seconds, people will go to another website.
  In an optimal solution, the browser would start downloading your scriptsas soon as possible, while at the same time parsing the rest of yourdocument.
  
  Before knowing the optimal solution , you must know how actually scriptfile treated by the browser, when browser load it -
  
  1.Fetch the HTML page (e.g. index.html) 
  2.Begin parsing the HTML 
  3.The parser encounters a <script> tag referencing an external scriptfile. 
  4.The browser requests the script file. Meanwhile, the parser blocksand stops parsing the other HTML on your page. 
  5.After some time the script is downloaded and subsequently executed.6.The parser continues parsing the rest of the HTML document. 
  Step   #4   causes   a   bad   user   experience.   Your   website   basically   stopsloading until you've downloaded all scripts. If there's one thing thatusers hate it's waiting for a website to load.

### The best and modern approach
Today, browsers support the async and defer attributes on scripts. Theseattributes tell the browser it's safe to continue parsing while thescripts are being downloaded.
 #### async
```
<script type="text/javascript" src="path/to/script1.js" async></script>
<script type="text/javascript" src="path/to/script2.js" async></script>
```
Scripts with the async attribute are executed asynchronously. This meansthe script is executed as soon as it's downloaded, without blocking the browser in the meantime.This implies that it's possible to script 2 is downloaded & executedbefore script 1. 
According   to   http://caniuse.com/#feat=script-async,   97.78%   of   allbrowsers support this

 #### defer
 ```
 <script type="text/javascript" src="path/to/script1.js" defer></script>
 <script type="text/javascript" src="path/to/script2.js" defer></script>
 ```
 Scripts   with   the   defer   attribute   are   executed   in   order   (i.e.   firstscript 1, then script 2). This also does not block the browser.Unlike async scripts, defer scripts are only executed after the entiredocument has been loaded.According   to   http://caniuse.com/#feat=script-defer,   97.79%   of   allbrowsers support this. 98.06% support it at least partially.

## Conclusion:
The current state-of-the-art is to put scripts in the <head> tag and usethe async or defer attributes. This allows your scripts to be downloadedasap without blocking your browser.The good thing is that your website should still load correctly on the2% of browsers that do not support these attributes while speeding upthe other 98%.

**[⬆  back to top](#lists-of-questions)**
## Contributors
* Sudhanshu Joshi - [SJoshi7](https://github.com/SJoshi7)
* Akshay Sharma - [AkshaySharma008](https://github.com/AkshaySharma008)
