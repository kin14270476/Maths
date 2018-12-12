#part 1 A
```c++
#include <iostream>
#include <random>
using namespace std;
int n1;
int n2;
int topanswer;
int botomanswer;
int finalanswer;
int GCD(int a, int b) 
{ 
    if (a == 0) 
        return b; 
    return GCD(b%a, a); 
} 

int main() 
{
  cout << "Please enter in how many buns:";
  while (!(cin >> n1)) 
  {
    cin.clear();
    cin.ignore(numeric_limits<streamsize>::max(),'\n');
    cout << "You did not enter in a number for the amount of buns. Please enter in a number: ";
  }
  cout << "Please enter in how many hot dogs:";
  while (!(cin >> n2))
  {
    cin.clear();
    cin.ignore(numeric_limits<streamsize>::max(),'\n');
    cout << "You did not enter in a number for the amount of hot dogs. Please enter in a number: ";
  }
  topanswer= n1 * n2;
  botomanswer= GCD(n1,n2);
  finalanswer= topanswer/botomanswer;
  cout << finalanswer;
}
```
