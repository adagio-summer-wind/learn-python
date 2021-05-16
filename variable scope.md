# LEGB rule
A variable resolution in Python follows the LEGB rule. That means that the interpreter looks for a name in the following order:<br>
>Locals: Variables defined within the function body and not declared global.<br>
>Enclosing: Names of the local scope in all enclosing functions from inner to outer.<br>
>Globals: Names defined at the top-level of a module or declared global with a global keyword.<br>
>Built-in: Any built-in name in Python.<br>
