Chocolate Distribution Problem in C++
 

Here, in this page we will discuss the Chocolate Distribution Problem in C++ Programming Language. We are given with an array of n integers these value represents the number of chocolates in a packet. Each packet can have a variable number of chocolates. There are m students, the task is to distribute chocolate packets such that: 

Every student gets one packet.
The difference between the number of chocolates in the packet with maximum chocolates and packet with minimum chocolates given to the students is minimum.
Chocolate Distribution Problem in C++
Algorithm :
First sort the array, using inbuilt sort() function.
Take a variable say mini = INT_MAX, so that it can store the required value.
Now, iterate over the entire array, and for every i-th element, find the difference between the a[i+m-1] and a[i], if it is minimum than mini value than set, mini to that difference.
After the complete iteration print the mini value.
Time and Space Complexity :
Time-Complexity : O(nlog(n))
Space-Complexity : O(1)
Chocolate Distribution Problem
Code for Chocolate Distribution Problem in C++
Run

#include<bits/stdc++.h>
using namespace std;

int main()
{
    int a[] = {7, 3, 2, 4, 9, 12, 56} ;
    int m = 3; 
    int n = sizeof(a) / sizeof(a[0]);
    int mini = INT_MAX;

   sort(a, a+n);

   for (int i = 0; i + m - 1 < n; i++) {
       int diff = a[i + m - 1] - a[i];
       if (diff < mini)
          mini = diff;
    }
    cout << "Minimum difference is "<< mini;
}
Output 

Minimum difference is 2
