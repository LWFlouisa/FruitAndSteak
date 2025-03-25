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

  // Fruits
  printf("Context 1. For the first row, the first fruits are %s.\n", fruit[0][0][0][1]); // First context, first row, first collumn, second item.
  printf("Context 1. For the first row, the second fruits are %s.\n", fruit[0][0][1][1]); // First context, first row, second collumn, second item. 
  printf("Context 1. For the first row, The third fruits are %s.\n", fruit[0][0][2][1]); // First context, first row, third collumns, second item.

  printf("Context 1. For the second row, the first fruits are %s.\n", fruit[0][1][0][1]);
  printf("Context 1. For the second row, the second fruits are %s.\n", fruit[0][1][1][1]);
  printf("Context 1. For the second row, the third fruits are %s.\n", fruit[0][1][2][1]);

  printf("Context 1. For the third row, the first fruits are %s.\n", fruit[0][2][0][1]);
  printf("Context 1. For the third row, the second fruits are %s.\n", fruit[0][2][1][1]);
  printf("Context 1. For the third row, the third fruits are %s.\n", fruit[0][2][2][1]);

  // Meats
  printf("Context 2. For the first row, the first meats are %s\n", fruit[1][0][0][1]);
  printf("Context 2. For the first row, the second meats are %s\n", fruit[1][0][1][1]);
  printf("Context 2. For the first row, the third meats are %s\n", fruit[1][0][2][1]);

  printf("Context 2. For the second row, the first meats are %s\n", fruit[1][1][0][1]);
  printf("context 2. For the second row, the second meats are %s\n", fruit[1][1][1][1]);
  printf("Context 2. For the second row, the third meats are %s\n", fruit[1][1][2][1]);

  printf("Context 2. For the third row, the first fruits are %s\n", fruit[1][2][0][1]);
  printf("Context 2. For the third row, the second fruits are %s\n", fruit[1][2][1][1]);
  printf("Context 2. For the third row, the third fruits are %s\n", fruit[1][2][2][1]);
}
~~~
