# EXP-14

## Aim:
**To study and implement Inheritance.**

## Software:
`Microsoft VSCode`

## Theory:
Constructor Overloading in C++ means that we have more than one constructor ina class with the same name, as long as each have a different list of arguments. A constructor is called depending upon the number and type of arguments passed.

While creating the object, arguments must be passed to let compiler know, which constructor needs to be called.
## Code: 14A
```
// NAME - Kanwaljeet singh
// PRN- 23070123124
// EXPERIMENT - 14(A) 

// Program to show single inheritance.

# include <iostream>
# include <string>
using namespace std;

class Uni
{
    public:
    string uni= "Symbiosis";
    void discipline()
    {
        cout << "Engineering" <<endl;
    }
};
class Dep : public Uni
{
    public:
    string dept= " Electronics & Telecommunication";
};
int main()
{
    Dep u1;
    u1.discipline();
    cout<<u1.uni + " "+u1.dept ;
} 
```
## Output:
![image](https://github.com/user-attachments/assets/52350e0d-7178-40c7-8783-0495033d26de)






## Code: 14B
```
// NAME - Kanwaljeet singh
// PRN - 23070123124
// EXPERIMENT - 14(B)

// Program toshow multiple inheritance.

#include<iostream> 
#include<string> 
using namespace std; 

// Parent CLass1 
class Vehicle {
    public:
    string company=" Ford";
    void type(){
        cout << "Mustang"<< endl;
    }
};
// Parent Class 2
class Specs{
    public:
    string mileage="8 kmpl";
    void colour(){
        cout<<"Grey"<<endl;
    }
};
// Child Class-1 (derived from parent- 1&2)
class Car: public Vehicle,public Specs{
    public:
    string seater = " 4 seater";
};
int main(){
    //multiple inheritance
    Car f2;
    f2.colour();
    cout<<f2.company<<" ";
    f2.type();
    cout<<"("<<f2.seater<<")"<<endl<<"MILEAGE:"<<f2.mileage<<endl;
} 

```

## Output:
![image](https://github.com/user-attachments/assets/4c027caf-32d0-4d1e-a8e0-fec0ed93cb46)



## Code: 14C
```
// NAME - Kanwaljeet singh
// PRN - 23070123124
// EXPERIMENT - 14(C)
// Program to showmultilevel inheritance.

#include<iostream> 
#include<string>
using namespace std; 

// single base class
class Student {
public:
    string stud;
    void get_Student_data()
    {
        cout << "Enter the name of the student: ";
        cin >>  stud;
    }
};
 
// derived class from base class
class PRN : public Student {
public:
    int prn;
    void get_PRN_data()
    {
        cout << "Enter the PRN: ";
        cin >> prn;
    }
};
 
// derived from class derive1
class Branch : public PRN {
private:
   string branch;
 
public:
    void get_Branch_data()
    {
        cout << "Enter the branch: ";
        cin >> branch;
    }
 
    // function to print sum
    void details()
    {
        cout << "Name: "<<stud<<"  PRN: "<< prn<<"  Branch: "<<branch << endl;
    }
};
int main()
{
    // object of sub class
    Branch obj;
 
    obj.get_Student_data();
    obj.get_PRN_data();
    obj.get_Branch_data();
    obj.details();
    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/2cae08d1-5e73-4964-99a3-f1bedbc3816a)

## Code: 14D
```
// NAME - Kanwaljeet singh
// PRN - 23070123124
// EXPERIMENT - 14(D)

// Program to show Hiererchical Inheritance.                    

#include <iostream>
using namespace std;

// base class
class Flower {
public:
    Flower() { cout << "This is a Flower. \n"; }
};

// first sub class
class Lotus : public Flower {
public:
    Lotus() { cout << "This flower is a lotus. \n"; }
};

// second sub class
class Marigold : public Flower {
public:
    Marigold() { cout << "Thisflower is a marigold. \n"; }
};

// main function
int main()
{
    // Creating object of sub class will invoke the constructor of base class.
    Lotus obj1;
    Marigold obj2;
    return 0;
}
```                  
## Output:
![image](https://github.com/user-attachments/assets/1af202f0-7806-4d4a-95fe-c4010721a666)


### Conclusion:
I learnt about inheritance in C++, its keywords, modes, types and performed programs based on that.
