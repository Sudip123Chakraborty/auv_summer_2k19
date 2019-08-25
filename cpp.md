
# SOME IMPORTANT KEYS
___
| |
|-|
|C++ STL|
___
## SET
* so in a set all the element will be in asorteed manner. 
* you need not sort the set .
* _In a set you can't insert any duplicat number ._<br />


|template|work|syntax|example|
|--------|----|-------|------|
|upper_bound|return the address of the element greater than it|s.upper_bound(x)| |
|lower_bound|return an iterator greater or equal to of that  element|s.lower_bound| |
___
int main()<br />
{<br />
set<int >s;<br />

s.insert(-5);<br />
s.insert(1);<br />
s.insert(-1);<br />
s.insert(5);<br />
auto it=s.upper_bound(-1);<br />
auto it1=s.lower_bound(-1);<br />

cout<<*it<<", "<<*it1;<br />
//ans = 1 , -1<br />
}
___

## substr()
In C++, std::substr() is a predefined function used for string handling. string.h is the header file required for string functions. <br />

This function takes two values pos and len as an argument and returns a newly constructed string object with its value initialized to a copy of a sub-string of this object. Copying of string start from pos and done till pos+len means [pos, pos+len).<br />

Important points:
___
   1. The index of the first character is 0 (not 1).
   1. If pos is equal to the string length, the function returns an empty string.
   1. If pos is greater than the string length, it throws out_of_range. If this happen, there are no changes in the string.
   1. If for the requested sub-string len is greater than size of string, then returned sub-string is [pos, size()).
___

___
// Take any string 
	string s1 = "Geeks"; 

	// Copy three characters of s1 (starting 
	// from position 1) 
	string r = s1.substr(1,3); 

	// prints the result 
	cout << "String is: " << r; 
  ___
## memset
memeset is used to fill block of memory<br />
* Time complexity O(n)<br />
```
// ptr ==> Starting address of memory to be filled
// x   ==> Value to be filled
// n   ==> Number of bytes to be filled starting 
//         from ptr to be filled
void *memset(void *ptr, int x, size_t n);
```
example:<br />
int arr[n]; <br />
memset(arr,0,n*sizeof(int));<br />
if n=10 it will be <br />
0 0 0 0 0 0 0 0 0 0<br />
___
## counting sort:([link](https://www.geeksforgeeks.org/counting-sort/))
* Assume all inputs to are intejer in[0,k]<br />
* Main logic is that count how many number are less than that number and placed it after that;
	* ie: if in array the number 5 is greater than 8 number than it's position in the sorted array will be 9.<br />
* Time complexity O(n+k)
* Spcae complexity O(n+k)
___
## radix sort:([link](https://www.geeksforgeeks.org/radix-sort/))
* counting sort take linear time complexity but if the digits are in range of [1,n*n] than it will take O(n*n)
time complexity.
* That time if we have to sort the array in linear time we can use **radix sort**`
```
Spcae complexity O(n+d)
Time complexity O(d*(n+b)
b=base for decimal representation it is 10
d=length of the largest number of the array
```
* if the value of k is to large it's time complexity become more that comparision based time complexity
___
## bucketsort([link](https://www.geeksforgeeks.org/bucket-sort-2/)):
```
bucketSort(arr[], n)
1) Create n empty buckets (Or lists).
2) Do following for every array element arr[i].
.......a) Insert arr[i] into bucket[n*array[i]]
3) Sort individual buckets using insertion sort.
4) Concatenate all sorted buckets.
```
## simultaneous min_max:
if we have to find the min and max of an array we can do it by (n-1)& (n-1) comparision<br />
**can we do it better?**<br />
* YES
* we process elements in pairs.  We compare pairs of elements from the inputfirstwith each other, and then we compare the smaller to the current minimum and thelarger to the current maximum, at a cost of 3 comparisons for every 2 elements.
	* If **n** is **odd**,  we set both the minimum and maximumto the value of the first element
	* If **n** is **even**, we perform 1 comparison on thefirst 2 elements to determine the initial values of the minimum and maximum, and then process the rest of the elements in pairs
