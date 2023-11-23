There are predefined macros in C:

- `__DATE__`: the current date as a string literal in "MMM DD YYYY" format;
- `__TIME__`: the current time as a string literal in "HH:MM:SS" format;
- `__FILE__`: the current filename as a string literal;
- `__LINE__`: the current line number as an integer;
- `__STDC__`: the value is 1 when the compiler complies with the ANSI standard

-------------------

## Stacktrace

the `__FILE__` and `__LINE__` macros can be used to create an stacktrace, which can help understand at what point a crash happened, for example.