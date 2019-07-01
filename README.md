# copy-constructor
//How to use make a copy constructor.
//This repository is for description of copy constuctor.A class already have an inbuilt copy constructor and it is called when values of //two objects are copied.Once it is created by you then validity of default copy constructor will die.
#include <iostream>

using namespace std;
class student{
public:
int rollno;
int age;
student(int rollno,int age)
{
    this -> rollno = rollno;
    this -> age = age;
}
student(const student &s)    //copy constructor.
{
    this -> rollno = s.rollno;
    this -> age = s.age;
}
void print()
{
    cout<<"AGE: "<<age<<" "<<"ROLL NUMBER: "<<rollno<<endl;
}

};
int main()
{
    student s1(7,18);
    s1.print();
    student s2(s1);
    s2.print();
    return 0;
}
