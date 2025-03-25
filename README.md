# FruitAndSteak
A 4D array in C.

## Concept
~~~
  //               0
  //          apples bananas kiwis
  // apples   a,a    a,b     a,k
  // bananas  b,a    b,b     b,k
  // kiwis    k,a    k,b     k,k

  //               1
  //          steak chicken fish
  // steak    s,s   s,c     s,f
  // chicken  c,s   c,c     c,f
  // fish     f,s   f,c     f,f
~~~

~~~c
#include <stdio.h>

int main() {
  char * fruit[2][3][3][2] = {
    {
      { {"apples",   "apples"}, {"apples",  "bananas"}, {"apples",    "kiwis"} },
      { {"bananas",  "apples"}, {"bananas", "bananas"}, {"bananas",   "kiwis"} },
      { {"kiwis",    "apples"}, {"kiwis",   "bananas"}, {"kiwis",     "kiwis"} },
    }, {
      { {"steak",   "steak"}, {"steak",   "chicken"}, {"steak",   "fish"} },
      { {"chicken", "steak"}, {"chicken", "chicken"}, {"chicken", "fish"} },
      { {"fish",    "steak"}, {"fish",    "chicken"}, {"fish",    "fish"} },
    }
  };

  printf("%s", fruit[0][0][0][0]);
  printf("%s", fruit[1][0][0][0]);
}
~~~
