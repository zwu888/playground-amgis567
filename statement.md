# description: 
 4 times. Virtual inheritance affects the class that is inherited virtually. Therefore the BS base class is not inherited virtually and there are 4 of them within 1 DR object. The virtual inheritance statements in this code are affecting the classes mid1, mid2, mid3, mid4 and not BS.
```C++ runnable
#include <iostream>

struct BS
{
  BS()
  {
    std::cout << "Hello World" << std::endl;
  }
};

struct mid1 : public BS { };
struct mid2 : public BS { };
struct mid3 : public BS { };
struct mid4 : public BS { };

struct DR : public virtual mid1, public virtual mid2, public virtual mid3, public mid4 { };

int main(int argc, char** argv) 
{ 
  DR d;
  return 0; 
}
```

