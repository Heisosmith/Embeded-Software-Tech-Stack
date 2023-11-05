# Embeded-Software-Tech-Stack
be to the senior embeded software engineer

## Table Of Contents
- Programming Languange
  - C
  - Python
  - Shell
- Data Structure And Algorithms
  - String
  - List
  - Queue
  - Tree/Heap
  - Hash Table
  - DAG
  - Sort
  - Search
  - Divide/Recursion/Iterate/DP
- Operating System
  - RTOS
  - Linux
- Fundamental
  - Circuit
  - Computer Organization And Architecture
- Peripheral Driver
  - Camera
- Software Architecture
  - Design Pattern
  - Unified Modeling Language
 
## C Language
C languages has small language set and simple grammer which easy to manster and use.
 
### Composition
- entity
  - literal
  - constant
  - variable
- operation
  - Arithmetic
  - Logic
  - Comparsion
  - Assignment
  - Bitwise
- flow control
  - select
  - repeat
  - jump
  - call

Data type of entity such as integer, float, char and pointer, just to indicate the type of value. The most important is tell compiler how much memory space to allocate to store the value. Literal have the entity with no named, it occupies memory space the same as entity named.

Operation is operating for operand, calculate or change the value of entity.

Generally, Program will execute all instruction one by one from start to end. Flow control use keyword to change the program execute flow / path. 
-  Select keyword (if-else) will do select one path to execute from multi-path, which mean skip some code that none be exeucted.
-  Repeat keryword (while) will do repeat one path multi-times.such like go back to execute / loop.
-  Jump keyword (goto/continue/break) will skip or terminate repeat, goto can jump to any instruction backed or fronted. goto fronted is repeat, goto backed is skip same code non executed.
-  Call keyword will enter sub-routine to execute instruction one by one, when it executed end, goto the next instruction after call sub-routine.

### Sample Code
```c
enum Gender
{
  MEM = 0;
  WOMEN = 1;
  OTHER = 2;
};

struct PersonInfo
{
  char[64] name;
  uint8_t  age;
  Gender   gender;
  float    height;
  float    weight;
};

int valid_info(struct PersonInfo params)
{
  if (params.name == "" ||
      params.age > 150 ||
      params.gender > 2 ||
      params.height > 300 ||
      params.weight > 200)
  {
    printf("Person Info Params has error \n");
    return -1;
  }
  return 0;
}

int main()
{
  struct PersonInfo mike { "Mike", 20, MAN, 188.5, 95.0 };
  struct PersonInfo jane { "Jane", 19, WOMEN, 173.0, 60.5 };

  ret = valid_info(mike);
  if (ret != 0)
    goto error_handle;

  loop_times = 0;
  while (loop_times < 2)
  {
    if (loops_times == 0)
    {
      printf("Name: %s \n Age %u \n Gender %u \n height %f \n weight %f \n",
              mike.name, mike.age, mike.gender, mike.height, mike.weight);
    }
    else if (loops_times == 1)
    {
      printf("Name: %s \n Age %u \n Gender %u \n height %f \n weight %f \n",
              jane.name, jane.age, jane.gender, jane.height, jane.weight);
    }
    else
    {
      break; // ternimate repeat
    }
    loop_times = loop_times + 1;
  }
  return 0;

error_handle:
  return -1;
}
```
