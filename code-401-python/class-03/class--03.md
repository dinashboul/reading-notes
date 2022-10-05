
# A beginner's guide to Big O Notation

## Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

#### You can visualize these functions and compare them:
 Name_____________Big O

Constant ________           O(c)

Linear ______       O(n)

Quadratic_____          O(n²)

Cubic_________      O(n³)

Exponential	_________           O(2ⁿ)

Logarithmic  ______        	O(log(n))

Log Linear	   _________         O(nlog(n))


![imge](./big-o-notation-and-algorithm-analysis-with-python-examples-1%20(1).png)

### O(1)

O(1) describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

> bool IsFirstElementNull (IList<String>elements)
>    return elements[0] == null;}

### O(N)

O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set
> bool ContainsValue(IEnumerable<string> elements, string value)

>{
    foreach (var element in elements)
    {
        if (element == value) return true; 
    }     
    return false; 
}

 ### O(N²)

 O(N²) represents an algorithm whose performance is directly proportional to the square of the size of the input data set.
 > bool ContainsDuplicates(IList<string> elements)
{
    for (var outer = 0; outer < elements.Count; outer++) 
    {
        for (var inner = 0; inner < elements.Count; inner++) 
        { 
            // Don't compare with self 
            if (outer == inner) continue;             
            
            if (elements[outer] == elements[inner]) return true; 
        }
    }    
    return false;}


### O(2^N)

O(2^N) denotes an algorithm whose growth doubles with each addition to the input data set.

>int Fibonacci(int number)
{
    if (number <= 1) return number;
       
    return Fibonacci(number - 2) + Fibonacci(number - 1); }

### Logarithms

Logarithms are slightly trickier to explain so I’ll use a common example:

Binary search is a technique used to search sorted data sets. 

This type of algorithm is described as O(log N). The iterative halving of data sets described in the binary search example produces a growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase e.g.

### In conclusion
Hopefully this has helped remove some of the mystery around Big O notation and many of the common growth functions. A grasp of Big O is an important tool when dealing with algorithms that need to operate at scale, allowing you to make the correct choices and acknowledge trade-offs when working with different data sets.

### References :
- Vaidehi Joshi,Saron Yitbarek,SEASON 1 EPISODE 6 NOVEMBER 29, 2017

