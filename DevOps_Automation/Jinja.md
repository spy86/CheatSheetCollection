This is a cheat sheet for the Jinja templating syntax.

## Syntax

The syntax is somewhat similar to ERB except for {} instead of <> quotes
```jinja
     {{ ... }}           # Escaping for expressions that create output
     {% ... %}           # Escaping for control statements
     # ... ##            # Line statements
``````jinja
## Loops
```jinja
     {% for i in list %} ... {% endfor %}
```
## Functions

Defining functions
```jinja
     {% macro myfunct(param1, param2) %}
     ...
     {% endmacro %}
 ```    
Using functions
```jinja
     {% myfunc(var, 5) %}
```
