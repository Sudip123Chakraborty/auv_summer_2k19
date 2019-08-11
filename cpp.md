
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
