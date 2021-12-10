# Dina153.github.io
## consts uses in c++ : 
1-Use const to tell others methods won't change the logical state of this object.
```
struct SmartPtr {
    int getCopies() const { return mCopiesMade; }
};
```
2-Use const for copy-on-write classes, to make the compiler help you to decide when and when not you need to copy.
```
 char * getData() { /* copy: caller might write */ return mData; }
    char const* getData() const { return mData; }
};
```
3-For the copy-constructor to make copies from const objects and temporaries
```
struct MyClass {
    MyClass(MyClass const& that) { /* make copy of that */ }
};
```
4-For making constants that trivially can't change
```
double const PI = 3.1415; 
```
5-For passing arbitrary objects by reference instead of by value
```
void PrintIt(Object const& obj) {
// ….
}
```
6-Const values 
 ```
 void PrintStudent(const Student& student) {
  cout << student.GetName();
}
 ```
7-Marking a member method as const
```
class Student {
  public:
    string GetName() const { ... }
};
```
8-You can use pointers to const data as function parameters to prevent the function from modifying a parameter passed through a pointer

9-You can specify the size of an array with a const variable 
## And (&) uses in c++ : 
1-We define a reference type by writing a declarator of the form &d, where d is the name being declared.
```
int* ptr=&num;//call by value 
```
2- the ref-sign (&) is used before the function name in the declaration of a function it is associated with the return value of the function and means that the function will return by reference.
```
int& foo(); // Function will return an int by reference
```
3- (&) compares each bit of the first operand to that bit of the second operand. If both bits are 1, the bit is set to 1. Otherwise, the bit is set to 0. Both operands to the bitwise AND operator must be of integral types.
```
int main() {  
   unsigned short a = 0x5555;      // pattern 0101 ...  
   unsigned short b = 0xAAAA;      // pattern 1010 ...  

   cout << hex << ( a & b ) << endl;

}
```
4-Uses in a conditional expression && 
```
if(a > b && a!=0 )
cout<< a << endl;
```
5-Use && for declaring universal references

6-Use && for declaring rvalue references

7-Use & or && for function overloading
