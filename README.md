# studious-octo-eureka
Write a function to calculate average marks of the class of one subject, declare an array to read marks of the students using new operator and delete after use. Display result in main function. 

#include<iostream>
using namespace std;
// Declaring function avg_marks
void avg_marks(int* marks)
{
// Initializing pointer variable as null
    int *total = NULL;
    total = new int;
    float *avg = NULL;
    avg = new float;
    *total = 0;

    for(int i= 0; i<3;i++)
    {
        cout<<"Enter marks"<<endl;
        cin>>*(marks+i);
        *total = *total + marks[i];
    }
    *avg = *total / 3;
    cout<<"the avg marks are "<<*avg<<endl;
    delete avg;
    delete total;
}
int main()
{
// Initializing pointer marks to null
    int* marks = NULL;
    marks = new int[3];
    avg_marks(marks);
    delete[] marks;
}
