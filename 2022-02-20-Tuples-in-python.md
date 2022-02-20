
Tuple:
* It is an ordered type as list but tuples are immutable.
* variable length input and output in tuples can be given as:
* ```
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







