# PHP ✨Magic ✨

## _All in One_

Table of contents.

- [How to install PHP](#how-to-install-php)
- [Print Variables](#how-to-print-variables)
- [Constants](#constants)
- [Magic Constants](#magic-constants)
- [Data Types](#data-types)
- [Arrays](#arrays)
- [Expressions](#expressions)
- [Operators](#operators)
- [Control Structures](#control-structures)
- [Loops](#loops)
- [Match](#match)
- [Tickable](#tickable)
- [Include Files](#include-files)
- [Splat Operator](#splat-operator)
- [Anonymous and Arrow Functions](#anonymous-and-arrow-functions)
- [PHP Configuration](#php-configuration)

## How to install PHP

### PHP Local Install

Installing PHP locally can be a great way to develop and test applications without having to deploy them to a live
server. However, there are some drawbacks to consider when installing PHP locally.

#### Pros

- Easy to set up and configure
- No need to deploy to a live server
- Can be used for development and testing

#### Cons

- Manual installation process
- Manual database installation
- Manual configuration of settings

### Software Bundles XAMPP/MAMP/WAMP

Software bundles such as XAMPP, MAMP and WAMP are great solutions for web development. They provide an all-in-one
solution that contains a web server, database, and is preconfigured for easy setup.

#### Pros

- All-in-one solution
- Contains web server
- Contains database
- Preconfigured for easy setup

### Virtual Machines

#### Pros

- Cost effective: Virtual machines are a cost-effective alternative to physical hardware, as they require fewer
  resources and can be easily scaled up or down.
- Flexibility: Virtual machines can be used for a variety of tasks, from web hosting to software development.
- Security: Virtual machines provide an extra layer of security, as they are isolated from the host system and other
  virtual machines.
- Portability: Virtual machines can be easily moved between different systems, making them ideal for cloud computing.

#### Cons

- Performance: Virtual machines can be slower than physical hardware, as they are sharing resources with other virtual
  machines.
- Complexity: Setting up and managing virtual machines can be complex and time consuming.
- Vulnerability: Virtual machines can be vulnerable to malware and other security threats, as they are connected to the
  internet.

## How to print variables

```php
echo "Batman";
// multiple
echo "Superman", "Batman";
```

`echo` is a language construct used to output one or more strings. It is a faster way to output data than using print.

```php
print "Superman";
// multiple
print "Batman "." Superman";
```

`print` is also a language construct used to output one or more strings. It is slower than echo, but it returns a value
of 1 which can be used in expressions.

## Constants

```php
define("HERO", "Superman");
```

`define()` is a PHP function used to define constants. It takes two parameters, the first being the name of the constant
and the second being its value. Constants defined using `define()` are global and can be accessed anywhere in the
script.

```php
const HERO = "Superman";
```

`const` is a keyword used to define constants in PHP. It works similarly to `define()`, but constants defined using
const are limited to the scope in which they are declared. They cannot be accessed outside of that scope. Additionally,
constants defined using const must be assigned a value at the time of declaration.

In summary, `define()` is used to define global constants while const is used to define local constants.

## Magic Constants

```php
__LINE__;
```

This magic constant returns the current line number of the file it is used in.

```php
__FILE__;
```

This magic constant returns the full path and filename of the file it is used in.

```php
__DIR__;
```

This magic constant returns the directory of the file it is used in.

```php
__FUNCTION__;
```

This magic constant returns the function name it is used in.

```php
__CLASS__;
```

This magic constant returns the class name it is used in.

```php
__TRAIT__;
```

This magic constant returns the trait name it is used in.

```php
__METHOD__;
```

This magic constant returns the method name it is used in.

```php
__NAMESPACE__;
```

This magic constant returns the namespace it is used in.

## Data Types

Scalar Types:

- Integer
- Float
- String
- Boolean

Compound Types:

- Array
- Object

Special Types:

- Resource
- NULL

**Type casting in PHP.** This is done by adding the desired type in front of the variable, e.g. `(int) $var`.

**Strict types** are a feature introduced in PHP 7 which forces type-checking on function arguments. This means that if
a function is declared with strict types enabled, it will only accept arguments of the specified type. If an argument of
a different type is passed, an error will be thrown. To enable strict types, add `declare(strict_types=1);` at the top
of the file.

## Arrays

1. Indexed Arrays:

```php
    $cars = array("Volvo", "BMW", "Toyota");
```

2. Associative Arrays:

```php
   $age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");
```

3. Multidimensional Arrays:

```php
  $cars = array (
      array("Volvo", 22, 18),
      array("BMW", 15, 13),
      array("Toyota", 5, 2)
  );
```

Short and faster way to push an element into an array

```php
  $heroes = [];
  $heroes[] = "Batman";
```

Working with arrays:

`print_r()` is a PHP function used to print out information about a variable in an easy-to-read format. It can be used
to print out arrays, objects, and other values.

`unset()` is a PHP function used to remove a variable or an element from an array. It will unset the variable or element
and make it undefined.

## Expressions

Expressions in PHP are a combination of variables, constants, and operators that evaluate to a value. They can be used
to assign values to variables, perform calculations, compare values, and more.

Examples of expressions in PHP include:

- Assigning a value to a variable: `$x = 5;`
- Performing a calculation: `$y = $x + 10;`
- Comparing two values: `if ($x == 5) { ... }`
- Using a ternary operator: `$z = ($x > 10) ? 'yes' : 'no';`

## Operators

- Assignment Operators:
  =, +=, -=, *=, /=, .=, %=, &=, |=, ^=, <<=, >>=
- String Operators:
  . (concatenation), .=
- Comparison Operators:
  ==, ===, !=, <>, !==, <, >, <=, >=
- Error Control Operators:
  @
- Increment/Decrement Operators:
  ++, --
- Logical Operators:
  and, or, xor, &&, ||, !
- Bitwise Operators:
  &, |, ~, ^, <<, >>
- Array Operators:
  +, ==, ===, !=, <>, !==
- Execution Operators:

```php
$command = `ls -a`;    
```

- Type Operators:

```php
$hero = new Hero();
$isHero = $hero instanceof Hero;
```

- Null Safe Operator (??)

The Null Safe Operator (??) is a new operator introduced in PHP 7. It is used to check if a value is null before
proceeding with the further operations. This operator is also known as the "Null Coalescing Operator".

```php
$name = $_GET['name'] ?? 'Guest';
echo "Hello $name";
```

- Operator Precedence & Associativity in PHP

| Operator | Description | Associativity |
| -------- | ----------- | ------------- |
| `()`     | Parentheses | Left-to-right |
| `**`     | Exponentiation | Right-to-left |
| `!`      | Not | Right-to-left |
| `*`, `/`, `%` | Multiplication, Division, Modulus | Left-to-right |
| `+`, `-` | Addition, Subtraction | Left-to-right |
| `<`, `<=`, `>`, `>=`, `<>` | Comparison | Left-to-right |
| `==`, `!=`, `===`, `!==` | Equality | Left-to-right |
| `&&`     | Logical AND | Left-to-right |
| &vert;&vert;   | Logical OR | Left-to-right |
| `?:`     | Ternary | Right-to-left |
| `=`, `+=`, `-=`, `*=`, `/=`, `%=` | Assignment | Right-to-left |
| `and`    | And | Left-to-right |
| `xor`    | Xor | Left-to-right |
| `or`     | Or | Left-to-right |

**Precedence** is the order in which operations are evaluated. In PHP, operators have a certain precedence and
associativity that determines the order in which operations are evaluated.

**Associativity** determines the order in which operations with the same precedence are evaluated. In PHP, operators are
either left-associative or right-associative. Left-associative operators are evaluated from left to right, while
right-associative operators are evaluated from right to left.

## Control Structures

* `if` statement - executes a set of code if a specified condition is true
* `else` statement - executes a set of code if the same condition is false
* `elseif` statement - executes a set of code if a different condition is true
* `switch` statement - selects one of many blocks of code to be executed

## Loops

* `for` loop - executes a block of code a specified number of times
* `foreach` loop - loops through a block of code for each element in an array
* `while` loop - loops through a block of code while a specified condition is true
* `do...while` loop - loops through a block of code once, and then repeats the loop while a specified condition is true
* `break` - used to break out of a loop
* `continue` - used to skip the current iteration of a loop and continue with the next iteration

## Match

**match** is a simpler regular expression syntax than **preg_match**, and is generally faster in PHP. It returns an
array of matches or false if no matches are found.

## Tickable

```php
// Register a tick function
declare(ticks=1);

// Function to be called on each tick event
function tick_handler()
{
    echo "tick_handler() called\n";
}

register_tick_function('tick_handler');

$a = 1;

if ($a > 0) {
    $a += 2;
    print($a . "\n");
}
```

The `tick` function in PHP is a callback function that is executed at the beginning of each tick. It is called after the
script is loaded and before any other code is executed. This allows for code to be executed at specific intervals, such
as every second or every minute.

The `tick` function can be used to perform tasks such as monitoring the system, logging events, or performing
maintenance tasks. It can also be used to execute code on a regular basis, such as checking for new data or updating a
database.

To use the `tick` function, it must first be registered with the `register_tick_function()` function. This function
takes a single parameter, which is the name of the function to be called. The `tick` function will then be called at the
start of each tick.

It is important to note that the `tick` function should not take too long to execute, as it will delay the execution of
the rest of the script. Additionally, the `tick` function should not produce any output, as this could interfere with
the output of the script.

## Include Files

| Function | Description |
| -------- | ----------- |
| include  | Includes and evaluates a specified file. |
| include_once | Includes and evaluates a specified file only once. |
| require  | Includes and evaluates a specified file. |
| require_once | Includes and evaluates a specified file only once. |

**Include**:

- If an error occurs, the script will continue to execute.

**Require**:

- If an error occurs, the script will stop executing.

## Splat Operator

The splat operator (`...`) is a new operator introduced in PHP 7. It allows for the expansion of an array into
individual parameters when calling a function.

For example, if you have an array `$arr = [1, 2, 3]`, you can use the splat operator to pass each element of the array
as a separate parameter to a function:

```php
function sum(...$numbers) {
    return array_sum($numbers);
}

$sum = sum(1, 5, 7, 9, 23);
```

## Anonymous and Arrow Functions

- Anonymous Functions in PHP

An anonymous function, also known as a closure, is a function that has no name and can be stored in a variable.
Anonymous functions are often used as callback functions, or for creating function scopes.

```php
$greet = function($name) {
    printf("Hello %s\r\n", $name);
};

$greet('World');
```

- Arrow Functions in PHP

Arrow functions are a shorthand syntax for writing anonymous functions in PHP. They allow you to write concise,
single-line functions that can be used as callbacks or passed as arguments to other functions.

```php
$add = fn($a, $b) => $a + $b;
echo $add(2, 3); // Outputs 5
```

## PHP Configuration

The `ini_get()` function is used to get the value of a configuration option from `php.ini`. It returns the value of the
configuration option as a string on success, or an empty string on failure.

`ini_set()` is a PHP function used to set a configuration option in the `php.ini` file at runtime. It allows you to change
the value of a configuration option without having to edit and save the `php.ini` file.