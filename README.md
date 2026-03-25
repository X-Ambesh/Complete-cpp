#### Number system in c++

```cpp
#include <iostream>
using namespace std;
int main() {
    int a = 15;
    int b = 017; // This is an octal literal, which is equal to 15 in decimal
    int c = 0x0F; // This is a hexadecimal literal, which is equal to 15 in decimal
    int d = 0b1111; // This is a binary literal, which is equal to 15 in decimal (C++14 and later)
    cout << "Decimal: " << a << endl;
    cout << "Octal: " << b << endl;
    cout << "Hexadecimal: " << c << endl;
    cout << "Binary: " << d << endl;    
    return 0;
}
```

#### int 

  - It occupies 4 bytes of memory 
  - It stores whole numbers (both positive and negative) without decimal points.
  
#### Variable braced initialization

```cpp
#include <iostream>
using namespace std;
int main() {
    int elephant_count; //Variable may contain random garbage value . Warning
    int lion_count {}; //Variable is initialized to zero
    int dog_count {10}; //Variable is initialized to 10
    int cat_count {10}; //Variable is initialized to 10
    // Can use expression as initializer
    int domestic_animals {dog_count + cat_count};
    // 2.9 is of type double , with a wider range than int. Error OR WARNING
    int narrow_initialization {2.9};
}
```
####  Funcion variabe intialization

```cpp
#include <iostream>
using namespace std;
int main() {
    int apple_cout(5);
    int orange_count(10);
    int fruit_count(apple_cout + orange_count);
    int narrow_initialization(2.9); // Information lost. less safe than braced initialization
    return 0;

}
```

#### Assignment Initialization

```cpp
int bike_count = 2;
int truck_count = 5;
int narrowing_conversion_assignment = 2.9; // Information lost. less safe than braced initialization
```

#### Size of a type in memory

```cpp
#include <iostream>
using namespace std;
int main() {
cout << "sizeof int: " << sizeof(int) << " bytes" << endl;
}
```

---
Unsigned range $[0 \sim  2^n - 1]$

Signed range $[-2^{n-1} \sim 2^{n-1} - 1]$

```cpp
int value0 {11}; // value0 can store both positive and negative values, as well as zero and occupies 4 bytes of memory
unsigned int value1 {10}; // value1 can only store positive values and zero occupies 4 bytes of memory
signed int value2 {-10}; // value2 can store both positive and negative values, as well as zero, and occupy the same amount of memory as value1 that is 4 bytes
```

---

#### To store fractional numbers


Type    | Size  |  Precision | comment
---------|----------|---------|-----------|
 float | 4 | 7 |-
 double | 8 | 15 | Recommended defalut
 long double | 12 | > double | -


>n(floating point) /0 = infinity(+ or -)
>
>0.0/0.0 = NaN (Not a Number)

---

#### bolean type

> Boolean type uses 8 bits i.e. 1 bytes of memory to store a value of either true or false. 

---

#### Characters and text

> Character literals are enclosed in single quotes (' ') and represent a single character. For example, 'A' represents the character A, and '1' represents the character 1. Character literals can also include escape sequences, such as '\n' for a newline or '\t' for a tab.

> It occupies 1 bytes in memory

```cpp
char letter {'A'}; // Character literal
char newline {'\n'}; // Escape sequence for newline
char value {65}; // ASCII value for 'A'
std ::cout << letter << newline; // Output: A (followed by a newline)
std ::cout << value << newline; // Output: A (followed by a newline)
```

--- 

#### auto 

> The auto keyword in C++ is used for type inference, allowing the compiler to automatically deduce the type of a variable based on its initializer. 

```cpp
auto var1 {12}; // var1 is deduced to be of type int
auto var2 {3.14}; // var2 is deduced to be of type double
auto var3 {'A'}; // var3 is deduced to be of type char
auto var4 {true}; // var4 is deduced to be of type bool
auto var5 {123u}; // var5 is deduced to be of type unsigned int
auto var6 {123ul}; // var6 is deduced to be of type unsigned long
auto var7 {123ll}; // var7 is deduced to be of type long long
```

---


#### `setw(x)`

> It is used to set width in output
> 
> for further left and right justified we can use
> 
> `std::right;`
> 
>` std::left; `
>
> `std::setfill("-")`
> 
>`std<<boolalpa;` to get true and false insted for 0 and 1
>
>`std::showpos;` it is used to show +ve sign in the output if the number is positive 
>
>`cout<<dec<<12;`
>
>`<cout<<hex<<100;`
>
> `std<<showbase;` it is used to show the base like 0xaf173 where 0x denotes hex
>
> `std<<upppercase;` for uppercase
>
> `std::<<steprecision(10)` it is used to set precision




| Manipulator(s)                         | Header       | Purpose                                              |
|---------------------------------------|-------------|------------------------------------------------------|
| std::endl                             | `<ostream>` | Insert new line character                            |
| std::flush                            | `<ostream>` | Flush the output stream                              |
| std::setw()                           | `<iomanip>` | Changes the width of the next input/output field     |
| std::left, std::right, std::internal  | `<ios>`     | Value justification                                  |
| std::boolalpha, std::noboolalpha      | `<ios>`     | Bool output format                                   |
| std::showpos, std::noshowpos          | `<ios>`     | Show + sign for positive numbers                     |
| std::dec, std::hex, std::oct          | `<ios>`     | Controls the default number system                   |
| std::showbase, std::noshowbase        | `<ios>`     | Include prefix to show base                          |
| std::uppercase, std::nouppercase      | `<ios>`     | Show digits in uppercase                             |


