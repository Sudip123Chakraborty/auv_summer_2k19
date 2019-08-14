
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
