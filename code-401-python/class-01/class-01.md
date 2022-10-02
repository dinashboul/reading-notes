# intro to Big O Notation

## a way to measure an algorithm's efficiency. It measures the time it takes to run your function as the input grows. Or in other words, how well does the function scale. There are two parts to measuring efficiency — time complexity and space complexity.

#### You can visualize these functions and compare them:
 Name	                 Big O
Constant	             O(c)
Linear	                 O(n)
Quadratic	             O(n²)
Cubic	                 O(n³)
Exponential	             O(2ⁿ)
Logarithmic            	O(log(n))
Log Linear	            O(nlog(n))

![imge](./big-o-notation-and-algorithm-analysis-with-python-examples-1%20(1).png)

### **Facts and Myths about Python names and values**

#### Python is simple
- Works like other languages
- Mechanisms are simple

#### names, values, assignment, and mutability in Python

- Names are refers to values 
 > x=5 
    print (x)
 the name “x” refers to the value 5. The next time we use the name x, we’ll get the value 5.

 - Many names can reffer to one values
 > x=4
 y=x
   x and y both refer to the same value

>Neither x or y is the “real” name. They have equal status: each refers to the value in exactly the same way.

 - Names are reassigned independently 
 >x=3

 >y=x

 >x=12
  If two names refer to the same value, this doesn’t magically link the two names. Reassigning one of them won’t reassign the other also.
   
- Values live until no references
- Assignment never copies data
> nums = [1, 2, 3]

>other = nums

> we assign nums to another name, we’ll have two names referring to the same list

-  change will be visible through all of the names
> nums = [1, 2, 3]

>other = nums
> nums.append(4)
>print(other)
> there was only ever one list, both names see the change. The assignment to other didn’t make a copy of the list, and the append operation didn’t copy the list before appending the value. There is only one list, and if you modify it through one of its names, the change will be visible through all of the names.

- Mutable  alising 
> - a mutable vlue
> -more than one name 
> - the value changes 
> - all names see the change 

- References can be more just names
>  nums = [1, 2, 3]
> x =num[1]

- Names have no type 
> values have no scope 
 >Just as names have no type, values have no scope. When we say that a function has a local variable, we mean that the name is scoped to the function: you can’t use the name outside the function, and when the function returns, the name is destroyed. But as we’ve seen, if the name’s value has other references, it will live on beyond the function call. It is a local name, not a local value.


## Bookmark and Review
- Ned Batchelder - Facts and Myths about Python names and values - PyCon 2015

- Vaidehi Joshi,Saron Yitbarek SEASON 1 EPISODE 6 NOVEMBER 29, 2017


