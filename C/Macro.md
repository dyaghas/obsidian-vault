#C

There are predefined macros in C:

- `__DATE__`: the current date as a string literal in "MMM DD YYYY" format;
- `__TIME__`: the current time as a string literal in "HH:MM:SS" format;
- `__FILE__`: the current filename as a string literal;
- `__LINE__`: the current line number as an integer;
- `__STDC__`: the value is 1 when the compiler complies with the ANSI standard

As macros are not part of the compilation process, but instead of the `preprocessor`, they are not supposed to be indented:

```C
#define MY_VAR 100

int main() {
	//here goes some code
#define MY_VAR_TWO 500
	//here goes some code
}
```

-------------------

## Stacktrace

the `__FILE__` and `__LINE__` macros can be used to create an stacktrace, which can help understand at what point a crash happened, for example.

------------------------

## Macro variables

A `macro variable` can be defined with the following sintax:

```C
#define VAR_NAME value

//example
#define MY_VAR 100
```

obs: macro variables are written in uppercase.

------------------------------
### Undef

This command can be used to clear a macro value, useful when another value for the same macro is wanted, for example.

```C
#undef VAR_NAME
```

----------------

## Function like macro

There are some situations where functions are not enough, for example, the code line 

```C
int array_len = sizeof(array) / sizeof(array[0]);
```

Cannot be used in a function to get array_len dinamically, that's because in this case, a function would get a pointer to this array as it's parameter, so it would be impossible to return its length without knowing the variable type beforehand.

For such cases, functions like macros can be used:

```C
#define CALC_ARRAY_len(x) (sizeof((x)) / sizeof((x)[0]))
```

**Why are there more brackets?** It is good practice to envelop every parameter in a function like macro.

If you need to choose between a function and a macro implementation of a library routine, consider the following trade-offs:

- `Speed versus size` - The main benefit of using macros is faster execution time. During preprocessing, a macro is expanded (replaced by its definition) inline each time it's used. A function definition occurs only once regardless of how many times it's called. Macros may increase code size but don't have the overhead associated with function calls.

- `Function evaluation` - A function evaluates to an address; a macro doesn't. Thus you can't use a macro name in contexts requiring a pointer. For instance, you can declare a pointer to a function, but not a pointer to a macro.  

- `Type-checking` - When you declare a function, the compiler can check the argument types. Because you can't declare a macro, the compiler can't check macro argument types; although it can check the number of arguments you pass to a macro.

----------------------

## Conditional compilation

The `#ifdef` keyword can be used to create macro conditionals. The code block inside it will only execute if the condition is true:

```C
#define MACRO_VAR 42

int main() {
	printf("Hello world\n");
#ifdef MACRO_VAR
	printf("MACRO_VAR is defined");
#endif
}
```

If `MACRO_VAR` is not defined, the line `printf("MACRO_VAR is defined")` won't be executed.

The `#if`, `#else` and `#elif` keyword can be used similarly to any other conditional.

```C
#define BUFFER_SIZE 124

int main() {
#if BUFFER_SIZE > 100
	printf("BUFFER_SIZE is bigger than 100");
#else
	printf("BUFFER_SIZE is not bigger than 100");
#endif
}
```

Note: in this case, the `else` clause also considers the case where BUFFER_SIZE is not defined. To solve that, do the following:

```C
#if defined BUFFER_SIZE && BUFFER_SIZE > 100
	printf("BUFFER_SIZE is bigger than 100");
#elif defined BUFFER_SIZE
	printf("BUFFER_SIZE is not bigger than 100");
#else
	printf("BUFFER_SIZE is not defined");
#endif
```