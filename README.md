# compile-time-string-format
a c++17 header library that implements a user-defined literals operator for a compile time string format.
### Example

```c++
#inculde "include/format.hpp"
#include <iostream>

int main()
{
    constexpr auto str = "/home/{}/folder/{}"_format("name"_s, "file1"_s);
    constexpr auto str2 = "{0}+{0} = {1}"_format("1"_s, 2_s);
    
    std::cout << str.c_str << std::endl;
    std::cout << str2.c_str << std::endl;
}
```
