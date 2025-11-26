# Ex.No:1
# Ex.Name: Write a CPP Program for Class to class conversion using casting operator(use character data).
## Date:
## Aim:
To write a C++ program demonstrating class-to-class conversion using a casting operator, where the source class contains a character and the target class stores it as a string or character member.

## Algorithm:
STEP 1: Start the program.

STEP 2: Create a source class ClassA with a private char data member.

STEP 3: Define a constructor in ClassA to initialize the character.

STEP 4: Create a target class ClassB with a private char or string data member.

STEP 5: In ClassA, define a type-cast operator to convert ClassA object to ClassB object.

STEP 6: Inside the casting operator, initialize a ClassB object with the character data from ClassA.

STEP 7: Return the ClassB object from the operator function.

STEP 8: Define a function in ClassB to display the character.

STEP 9: In the main() function, create an object of ClassA.

STEP 10: Convert the ClassA object to ClassB object using the casting operator and display the value.




## Program:
```
#include <bits/stdc++.h>
using namespace std;

class Class_type_one
{
    string a;  
public:
    Class_type_one(string str) : a(str) {}

    string get_string() 
    {
        return a;
    }

    void display()
    {
        cout << a << endl;
    }
};

class Class_type_two
{
    string b;  

public:
    Class_type_two() {}

    Class_type_two(Class_type_one &objA)
    {
        b = objA.get_string();
    }

    void display()
    {
        cout << b << endl;
    }
};

int main()
{
    string a;
    cin>>a;
    Class_type_one objA(a);

    Class_type_two objB = objA;

    objA.display();
    objB.display();

    return 0;
}

```


## Output:
<img width="448" height="315" alt="{AC553189-F9E9-4656-94C7-D68832F43E31}" src="https://github.com/user-attachments/assets/169441ef-b92e-4ec3-93bb-869f82fa740d" />



## Result:
Thus, the program successfully demonstrates class-to-class conversion using a casting operator with character data.
