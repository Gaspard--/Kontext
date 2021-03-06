# Kontext

The language is parsed in a top-down matter during compilation.
Different operations are possible:
- Type declartion
  ```
  type A = int;
  ```
- Struct declaration
  ```
  struct B =
  {
    A donuts;
    int dogs;
  };
  ```
- Constant declaration
  ```
  A a = 5;
  ```
- Function declaration
  ```
   function a(A b)
    = 5 * b;
   function Pair(Type A)
    = return {A, A};
  ```
  
  Note: Types, Structs and Constants can be used as functions that take no parameters
- Lambda declaration
  ```
  function times(A b, A c)
    = b * c;
  lambda fiveTimes = a(5);
  ```

- Interface declaration (series of accessors)
  ```
  interface Dog = {
    function mouse(A a, B b) = a * b;
    function cat(A a) -> A = a;
  }
  ```

- Object declaration
  ```
  dogTwo = Dog(2);
  ```

- Functor declaration (Compute an interface from other interfaces)
  ```
  functor Dog dog
    Interface Horse
      function deer = Dog.cat
  ```
  
