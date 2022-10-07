# CPP by Example

## C++ Absolute Value

The C++ Standard Library provides the abs function which returns the absolute value of its only argument. For example:

```cpp
#include <cmath>
#include <iostream>
int main() {
  auto result = std::abs(-3.141592f);
  std::cout << result << "\n";
  auto result2 = std::abs(42);
  std::cout << result2 << "\n";
}
```

## How to Add to an Array

In C++ arrays are fixed size, meaning you cannot change the array’s size after creating it. Arrays that can change their size are known as std::vector in C++. To add to a std::vector you use the push_back method. In other languages this may be called append or push.

```cpp
#include <vector>
#include <iostream>
int main() {
  std::vector<int> v;
  v.push_back(42);
  std::cout << v.size() << "\n";
  std::cout << v.back() << "\n";
}
```

## How to Append to Strings

You can append to std::string with the append method or the addition assignment operator(+=). Both are just as good.

```cpp
#include <string>
#include <iostream>
int main() {
  std::string sentence{"She"};
  sentence.append(" is playing");
  sentence += " the piano.";
  std::cout << sentence << "\n";
}
```

## How to Concatenate Strings

std::string implements concatentation via the addition operator (+).

```cpp
#include <string>
#include <iostream>
int main() {
  std::string subject{"She"};
  std::string verb{"is playing"};
  std::string object{"the piano"};
  std::string sentence = subject + " " + verb + " " + object + ".";
  std::cout << sentence << "\n";
}
```

## What is Const

Variables in C++ are mutable, meaning they can change their values over time. To declare a variable as immutable, or unchanging, in C++ we use const.

```cpp
#include <string>
#include <iostream>
int main() {
  const int x = 42;
  const std::string name = "Rainier";
  std::cout << x << " " << name << "\n";
}
```

```cpp
#include <string>
#include <iostream>
void print_name(const std::string& name) {
  std::cout << name << "\n";
}
int main() {
  std::string name = "Rainier";
  print_name(name);
}
```