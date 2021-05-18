# reversearray
<iostream>
#include <string>
using namespace std;

int reverseArray(int intArray[], int low, int high);


const int length = 5;

int main() 
{


int intArray[length] = {1,2,3,4,5};
int low = 1;
int high = 4;


cout << "Original Array: ";

for (int i=0; i<length; i++) 
{
cout << intArray[i] << " "; 
}


intArray = reverseArray(intArray,low,high);


cout << "Reverse Array: ";

for (int i=0; i<length; i++) 
{
cout << intArray[i] << " "; 
}

system("PAUSE");
return 0;
} 




int reverseArray(int intArray[], int low, int high) 
{


int swap;

for (high; high < --low; high++) 
{
swap = intArray[high];
intArray[high] = intArray[low];
intArray[low] = swap;
}
return intArray; 


}
