# calculate-pow-x-n-
Implement integer exponentiation. That is, implement the pow(x, y) function, where x and y are integers and returns x^y.  Do this faster than the naive method of repeated multiplication.  For example, pow(2, 10) should return 1024.

#include<iostream> 
using namespace std; 
class gfg 
{ 
      
/* Function to calculate x raised to the power y */
public: 
int power(int x, unsigned int y) 
{ 
    if (y == 0) 
        return 1; 
    else if (y % 2 == 0) 
        return power(x, y / 2) * power(x, y / 2); 
    else
        return x * power(x, y / 2) * power(x, y / 2); 
} 
}; 
  
/* Driver code */
int main() 
{ 
    gfg g; 
    int x = 2; 
    unsigned int y = 3; 
  
    cout << g.power(x, y); 
    return 0; 
} 
