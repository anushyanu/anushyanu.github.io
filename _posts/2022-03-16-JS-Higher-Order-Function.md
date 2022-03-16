Higher order functions:
  * The function can be passed in the input as a argument.
  e.g function add(a,b){
        return a + b;}
      function subtract(a,b){
        return a - b ;}
      function calculator(x,y,operator){
        return operator(x,y);}  
  calling a func:
      calculator(2,3,add)   --> here the operator goes to the specific function
      
  * It can be as a anonymous function.
