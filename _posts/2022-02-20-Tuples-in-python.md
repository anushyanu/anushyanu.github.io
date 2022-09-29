Python Basics:

     * In storing values in memory if 
     a = 10 --> a points the value 10 to some memory address 
     a = (a + 1) is 11 --> a points the value to different memory address
     Now if we get the the value of a ,result is 11.
 
     * If a = 10, b = 10 then both gets stored in same place becoz of optimization 
     * Different Variables can be stored in same place from -5 to 255.
     e.g a =100 , b = 100.
     
     * Continue statement--> it immediately goes to the loop when it see continue
     
     * Break statement --> it breaks from the loop when you give break.
     
     * Pass statement --> it used to write the dummy statement in if condition 
     
     
   
Lists:
     
     Pop:
     It is used to take the last index out
     e.g li = [1,2,3] 
         li.pop() -->[1,2]
        
     Remove:
     It is used to take any element out by specifying it.
     e.g li =[1,2,3]
        li.remove(2) -->[1,3]
     * Python store any datatypes in lists.
     
     
Taking Inputs in Lists:

     Line separated input list 
     ```
     given:
     1
     2
     3
     li=[]
     for i in range(n):
          curr = int(input())
          li.append(curr)
     o/p : li = [1,2,3]
     
     ```
     Space separated input list
     
     given:
     ``` 
     s = '1 2 3 4'
     
     input.split(" ") so it gives s = ['1','2','3','4']
     
     It can be written in one line 
     
     li = [int(x) for x in input().split(" ")]
     
     o/p:li =[1,2,3,4]
     
     
     
     
Tuple:

     * It is an ordered type as list but tuples are immutable.
     * variable length input and output in tuples can be given as:
      ```
     def sum(a,b,*more):
        sum=a+b
        for i in more:
            sum=sum+i
        return sum
    sum(2,3,4,5,6)
     ```
     output:20
     Here, the *more take the argument of 4,5,6.

     *Tuples with some examples:
 ```
      def sum_diff(a,b):
        return a+b,a-b,a*b
      d,e,f = sum_diff(1,2)
  
```
     Output: get an error, because the variable length should be same as the output or one variable can be used which is being created as Tuple.


Global and local variable in function:

     global variable:
     ```
     y = 10
     def num():
          y = 2
          print(y)
     print(y)
     num()
     print(y)
     
     o/p : 10
           2
           10
     ```
     
    To access the local variable which is inside the functon, should use global y
    ```
    y = 10
    def num():
          global y
          y = 2
          print(y)
    print(y)
    num()
    print(y)
    
    o/p : 10
          2
          2
    ```



