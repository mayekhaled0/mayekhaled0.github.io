# Task3

## A) Usages of Const keyword
### 1) Constant variables:

We can declare constant variables using const keyword, we cannot change its value, and it must be initialized when it is declared.
ex:
       
~~~cpp  
int main
{
    const int minutesPerHour = 60;
    const float pi = 3.14;  
}

~~~


### 2) Pointers with const keyword:
We can apply const keyword to what the pointer is pointing to, or we can make the pointer itself a constant.
     
ex(1):
       
~~~cpp
         const int* num; //the pointer is pointing to a constant variable.
~~~

Pointers to a const variable is useful as it can be used to make any string or array immutable.
     
ex(2): 
       
~~~cpp
         int x = 1;
         int* const ptr = &x; //constant pointer
~~~

The constant pointer to a variable is useful where you want a storage that can be changed in value but not moved in memory because the pointer will always point to the same memory location.

### 3) Defining Class data members as const:
Data variables in class which are defined using const keyword are not initialized during declaration,but their initialization is done in the constructor.
ex: 
       
~~~cpp
            class Test 
           {
           const int i;
           public:
           Test(int x):i(x)
           {
            cout << "\ni value set: " << i;
           }
           };
           
           int main()
           {
            Test t(10);
            Test s(20);
            }
~~~
  

### 4) const Function Arguments and Return types:
We can make the return type or arguments of a function as const, so we cannot change any of them.
ex(1):
       
~~~cpp 
     const int g()
        {
          return 1;
        } //constant return type
~~~

ex(2):
        
~~~cpp
     void fun(const int i)
     {
       i++; //error because we cannot edit the value of i
     }
~~~

### 5) Defining Class Object as const:
If an object is declared/created using the const keyword, its data members can never be changed.
ex: 
        
~~~cpp
         const Test x(10); //object x has constant value
~~~

### 6) Defining Class's member functions as const:
A const member functions never modifies data members in an object.
ex: 
        
~~~cpp
     int getValue() const 
            {
             return value; 
             }
~~~

## B) Usages of "&"

### 1) Bitwise AND operator:
The bitwise AND operator (&) compares each bit of the first operand to that bit of the second operand. If both bits are 1, the bit is set to 1. Otherwise, the bit is set to 0. 
ex:
        
 ~~~cpp
            int main() 
            {
              int a = 5, b = 9;  // a = 5(00000101), b = 9(00001001)
              cout << "a & b = " << (a & b) << endl;   // The result is 00000001
            }
~~~

### 2) Address of operator:
An address-of operator returns the memory address of a variable "pointers".
ex: 
         
~~~cpp 
        int main () 
            {
           int  var;
           int  *ptr;
           int  val;

           var = 3000;

           ptr = &var;    // take the address of var
        }
~~~
