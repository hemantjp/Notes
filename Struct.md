typedef struct {
  int x, y;
} Point;

Point point_new(int x, int y)
{
  Point a;
  a.x = x;
  a.y = y;
  return a;
}

The common idiom is using both:

typedef struct S { 
    int x; 
} S;

They are different definitions. To make the discussion clearer I will split the sentence:

struct S { 
    int x; 
};

typedef struct S S;

In the first line you are defining the identifier S within the struct name space (not in the C++ sense). You can use it and define variables or function arguments of the newly defined type by defining the type of the argument as struct S:

void f( struct S argument ); // struct is required here

The second line adds a type alias S in the global name space and thus allows you to just write:

void f( S argument ); // struct keyword no longer needed

Note that since both identifier name spaces are different, defining S both in the structs and global spaces is not an error, as it is not redefining the same identifier, but rather creating a different identifier in a different place.

To make the difference clearer:

typedef struct S { 
    int x; 
} T;

void S() { } // correct

//void T() {} // error: symbol T already defined as an alias to 'struct S'

You can define a function with the same name of the struct as the identifiers are kept in different spaces, but you cannot define a function with the same name as a typedef as those identifiers collide.

In C++, it is slightly different as the rules to locate a symbol have changed subtly. C++ still keeps the two different identifier spaces, but unlike in C, when you only define the symbol within the class identifier space, you are not required to provide the struct/class keyword:

 // C++
struct S { 
    int x; 
}; // S defined as a class

void f( S a ); // correct: struct is optional

What changes are the search rules, not where the identifiers are defined. The compiler will search the global identifier table and after S has not been found it will search for S within the class identifiers.

The code presented before behaves in the same way:

typedef struct S { 
    int x; 
} T;

void S() {} // correct [*]

//void T() {} // error: symbol T already defined as an alias to 'struct S'

After the definition of the S function in the second line, the struct S cannot be resolved automatically by the compiler, and to create an object or define an argument of that type you must fall back to including the struct keyword:

// previous code here...
int main() {
    S(); 
    struct S s;
}


