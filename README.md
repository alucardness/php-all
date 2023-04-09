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
- [Errors](#errors)
- [Error Handling](#error-handling)
- [Working with Files](#working-with-files)
- [Setup Project](#setup-project)
- [Coding Standards, Autoloading and Composer](#coding-standards-autoloading-and-composer)
- Objects
    - [Chaining Methods](#chaining-methods)
    - [Constructor Property Promotion](#constructor-property-promotion)
    - [Constants](#constants)
    - [Static Properties and Methods](#static-properties-and-methods)
    - [Encapsulation and Abstraction](#encapsulation-and-abstraction)
    - [Abstract Classes and Methods](#abstract-classes-and-methods)
    - [Interfaces and Polymorphism](#interfaces-and-polymorphism)
    - [Magic Methods](#magic-methods)
    - [Late Static Binding](#late-static-binding)
    - [Traits](#traits)
    - [Anonymous Class](#anonymous-class)
    - [Clone Objects](#clone-objects)
    - [Serialize Objects](#serialize-objects)
    - [Iterate Over Objects](#iterate-over-objects)
- [DocBlock](#docblock)
- [Exceptions](#exceptions)

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

`ini_set()` is a PHP function used to set a configuration option in the `php.ini` file at runtime. It allows you to
change the value of a configuration option without having to edit and save the `php.ini` file.

## Errors

### Types of Errors

1. **Parse Error**: This occurs when the syntax of a code is incorrect.
2. **Fatal Error**: This occurs when a critical error causes the program to stop unexpectedly.
3. **Warning Error**: This occurs when there is an issue with the code, but it does not cause the program to stop.
4. **Notice Error**: This occurs when the code encounters an unexpected condition that is not necessarily an error.
5. **Strict Error**: This occurs when the code encounters a deprecated feature or an incompatible API usage.
6. **Recoverable Error**: This occurs when the code encounters an error that can be recovered from.

## Error Handling

Show all Errors

```php
ini_set('display_errors', 1);
ini_set('display_startup_errors', 1);
error_reporting(E_ALL);
```

Customer Error Hanlder

```php
// Custom error handler function
function customError($errno, $errstr) {
  echo "<b>Error:</b> [$errno] $errstr<br>";
  echo "Ending Script";
  die();
}

// Set error handler
set_error_handler("customError");

// Trigger error
echo($test);
```

## Working with Files

- Create Folder

```php
$folderName = 'myFolder';
if (!is_dir($folderName)) {
    mkdir($folderName, 0777, true);
}
```

- Delete Folder

```php
$folderName = 'myFolder';
if (is_dir($folderName)) {
    rmdir($folderName);
}
```

- Read File

```php
$fileName = 'myFile.txt';
$fileHandle = fopen($fileName, 'r');
$fileContent = fread($fileHandle, filesize($fileName));
fclose($fileHandle);
echo $fileContent;
```

- Delete File

```php
$fileName = 'myFile.txt';
if (file_exists($fileName)) {
    unlink($fileName);
}
```

## Setup Project

- Docker
    - file structure

    ```
    ├── src/
    │   ├── index.php
    │   └── ...
    └── docker/
        ├── docker-compose.yaml
        ├── nginx/
            └── nginx.conf
        └── Dockerfile
    ```

    - Docker file
    ```dockerfile
        FROM php:8.0.2-fpm

        RUN apt-get update && apt-get install -y \
            git \
            curl \
            zip \
            unzip
        
        WORKDIR /var/www
    ```

    - nginx.conf
    ```nginx configuration
        server {
            listen 80;
            index index.php;
            error_log /var/log/nginx/error.log;
            access_log /var/log/nginx/access.log;
            error_page 404 /index.php;
            root /var/www/public;
            location ~ \.php$ {
                try_files $uri =404;
                fastcgi_pass app:9000;
                fastcgi_index index.php;
                include fastcgi_params;
                fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
            }
            location / {
                try_files $uri $uri/ /index.php?$query_string;
                gzip_static on;
            }
        }
    ```

    - docker-compose.yaml
    ```yaml
        version: '3.8'
  
        services:
          app:
            build:
              context: ./
              dockerfile: Dockerfile
            container_name: php-framework-app
            restart: always
            working_dir: /var/www/
            volumes:
              - ../src:/var/www
        
          nginx:
            image: nginx:1.19-alpine
            container_name: php-hero-container
            restart: always
            ports:
              - "8000:80"
            volumes:
              - ../src:/var/www
              - ./nginx:/etc/nginx/conf.d
    ```

## Coding Standards, Autoloading and Composer

- Autoloading and Composer

1. Install composer.
2. Include the autoloader.

```php
require_once __DIR__ . '/vendor/autoload.php';
```

3. Touch the composer.json file to automatically load all classes from app folder.

```composer
  "autoload": {
    "psr-4": {
      "App\\": "app/"
    }
  }
```

4. Clear the Composer's cache.

```shell
composer dump-autoload
```

## Objects

### Chaining Methods

```php
class MyClass {
  public function method1() {
    // do something
    return $this;
  }
  
  public function method2() {
    // do something
    return $this;
  }
}

$myObject = (new MyClass());
$myObject->method1()->method2();
```

Chaining methods in PHP is a technique used to call multiple methods on an object or class in a single statement. This
allows for more concise and readable code, as well as improved performance due to fewer lines of code being executed.

To chain methods, the return value of one method must be an object or class that can accept the next method in the
chain.

### Constructor Property Promotion

```php
class Customer
{
    public function __construct(
        public string $name, 
        public string $email, 
    ) {}
}
```

Constructor property promotion is a feature of PHP that allows developers to assign values to class properties directly
in the constructor. This eliminates the need to write out each property assignment individually, making code more
concise and easier to read.

**Available from php >= 8.0**

### Constants

```php
class Hero {
  const HERO_NAME = 'Superman';
  const HERO_POWER = 'Flight';
  const HERO_WEAPON = 'Heat Vision';
  private const HERO_SECRET = 'Kryptonite';
  
  public function getSecret() {
    return self::HERO_SECRET;
  }
}

echo Hero::HERO_NAME; // Superman
echo Hero::class; // call class's full path
```

### Static Properties and Methods

```php
class Hero {
  // Static property
  public static $universe = 'Marvel';
  
  // Static method
  public static function getUniverse() {
    return self::$universe;
  }
}

// Accessing static property
echo Hero::$universe; // Outputs: Marvel

// Accessing static method
echo Hero::getUniverse(); // Outputs: Marvel
```

Static properties and methods in PHP are class members that can be accessed without creating an instance of the class.
They are declared using the static keyword, and they can be accessed using the scope resolution operator (::). Static
properties and methods can be used to store and access data that is shared across all instances of a class.

Static properties and methods can be used in a variety of ways in PHP. Here are some common use cases:

1. Keeping track of global state: Static properties and methods can be used to keep track of global state, such as the
   number of times a certain function has been called or the total number of objects created.

2. Creating utility functions: Static methods can be used to create utility functions that don't need to be
   instantiated. For example, a static method could be used to generate a random string or check if a given value is
   valid.

3. Caching data: Static properties can be used to cache data that doesn't change often, such as configuration settings
   or database query results. This can help improve performance by avoiding unnecessary database queries or
   calculations.

4. Implementing singleton classes: Static methods can be used to implement singleton classes, which are classes that can
   only have one instance at any given time. This can be useful for implementing global objects, such as a logger or a
   configuration manager.

### Encapsulation and Abstraction

- Encapsulation in PHP is the process of combining properties and methods into a single class. This allows for data to
  be protected from outside access, while still allowing the class to be used by other classes or functions.
  Encapsulation also helps to reduce code complexity and improve code readability. It is an important concept in
  object-oriented programming (OOP).

```php
class Hero {
  // Private properties
  private $name;
  
  // Constructor
  public function __construct($name) {
    $this->name = $name;
  }
  
  // Getters and Setters
  public function getName() {
    return $this->name;
  }
  
  public function setName($name) {
    $this->name = $name;
  }
}
```

_Setters are considered bad practice because they can lead to code that is difficult to maintain and debug. Setters
allow for the state of an object to be changed without any validation or control, which can lead to unexpected results
and errors. Additionally, setters can make it difficult to track changes to an object's state over time, as there is no
record of when and how the state was changed._

- Abstraction

_Abstraction in PHP is the process of hiding the implementation details from the user, only the functionality will be
provided to the user._

### Abstract Classes and Methods

```php
// Abstract class for Hero objects
abstract class Hero {
  // Protected properties of the Hero object
  protected $name;
  protected $health;
  protected $power;
  
  // Constructor to set up the Hero object
  public function __construct($name, $health, $power) {
    $this->name = $name;
    $this->health = $health;
    $this->power = $power;
  }
  
  // Abstract method to be implemented by subclasses
  abstract public function attack();
}
```

_An abstract class in PHP is a class that cannot be instantiated, and must be extended by another class. Abstract
classes are used to provide a base level of functionality that can be shared among multiple classes. They may contain
abstract methods, which are methods without any implementation, and must be implemented by the extending class._

### Interfaces and Polymorphism

Abstraction classes and interfaces are both used to define abstractions in PHP. An abstraction class is a class that
contains abstract methods, which must be implemented by any class that extends it. An interface is a contract between
two objects, specifying that certain methods must be implemented by the implementing object.

_Polymorphism in PHP is the ability of an object to take on different forms depending on the context. This allows for
code reuse and flexibility when dealing with different types of objects. For example, a function may accept an object as
an argument and then call different methods depending on the type of object passed in._

### Magic Methods

```php
// Constructor method
__construct()

// Destructor method
__destruct()

// Magic method that is triggered when invoking inaccessible methods in an object context
__call()

// Magic method that is triggered when invoking inaccessible methods in a static context
__callStatic()

// Magic method for getting properties of an object
__get()

// Magic method for setting properties of an object
__set()

// Magic method to check if a property is set
__isset()

// Magic method to unset a property
__unset()

// Magic method to prepare an object for serialization
__sleep()

// Magic method to wake up an object after deserialization
__wakeup()

// Magic method to return the string representation of an object
__toString()

// Magic method to allow an object to be called as a function
__invoke()

// Magic method to control object serialization
__set_state()

// Magic method to clone an object
__clone()

// Magic method to return debugging information about an object
__debugInfo()
```

### Late Static Binding

```php
class Hero {
    public static function battleCry() {
        echo "FIGHT!";
    }
}

class SuperHero extends Hero {
    public static function battleCry() {
        echo "IT'S HERO TIME!";
    }
}

$hero = new Hero();
$hero::battleCry(); // Outputs: IT'S HERO TIME!
```

_Late static binding in PHP is a feature that allows static methods to be called on a class that is determined at
runtime. This allows for more flexibility when dealing with inheritance, as it allows the child class to call the parent
class's static methods without having to explicitly specify the parent class. It also allows for more dynamic code, as
the class being called can be changed depending on the context._

### Traits

```php
trait Logger {
    public function log($message) {
        echo $message;
    }
}
 
class User {
    use Logger;
    
    public function login() {
        $this->log('User logged in');
    }
}
```

_The purpose of a trait in PHP is to provide a way to reuse code between classes. Traits allow you to define methods
that can be used in multiple classes without having to copy and paste the same code into each class. In the example
above, the Logger trait provides a log() method which can be used by the User class without having to define it again._

- Calling a method that exists in at least two traits

```php
trait heroFly
{
    public function getSpeed()
    {
        $speed = rand(1, 10);
        return "Hero speed: " . $speed;
    }
}

trait villainFly
{
    public function getSpeed()
    {
        $speed = rand(11, 20);
        return "Villain speed: " . $speed;
    }
}

class Hero
{
    use heroFly, villainFly {
        villainFly::getSpeed insteadof heroFly;
    }

    public function getHeroSpeed(): string
    {
        return $this->getSpeed();
    }
}

$superman = new Hero();
echo $superman->getHeroSpeed();
```

### Anonymous Class

```php
$hero = new class {
  public $name;
  public $age;
  public $superpower;
  
  public function __construct($name, $age, $superpower) {
    $this->name = $name;
    $this->age = $age;
    $this->superpower = $superpower;
  }
};
```

_Anonymous classes in PHP are used to create objects without having to define a class first. This can be useful for
creating simple, one-off objects that don't need to be reused or extended. Anonymous classes can also be used to quickly
mock objects for testing purposes._

### Clone Objects

```php
class Hero {
  public $name;
  public $id;
  
  public function __construct($name) {
    $this->name = $name;
    $this->id = uniqid();
  }
  
  public function __clone() {
    $this->id = uniqid();
  }
}

$hero1 = new Hero('Superman');
$hero2 = clone $hero1;

echo $hero1->id . '<br>';
echo $hero2->id;
```

_The `__clone()` method is used to create a clone of the object and assign it a new unique id._

### Serialize Objects

_The purpose of serializing objects in PHP is to convert an object into a string representation, which can then be
stored in a database or file, and later retrieved and converted back into an object. This allows for the object's state
to be preserved across multiple requests._

### Iterate over Objects

```php
class Hero
{
    public $name;
    public $power;
    public $weapon;

    public function __construct($name, $power, $weapon)
    {
        $this->name = $name;
        $this->power = $power;
        $this->weapon = $weapon;
    }
}

$heroes = [
    new Hero('Superman', 'super strength', 'heat vision'),
    new Hero('Wonder Woman', 'superhuman strength', 'lasso of truth'),
    new Hero('Batman', 'genius-level intellect', 'utility belt')
];

class HeroesCollection implements IteratorAggregate
{
    private $heroes;

    public function __construct($heroes)
    {
        $this->heroes = $heroes;
    }

    public function getIterator()
    {
        return new ArrayIterator($this->heroes);
    }
}

$heroesCollection = new HeroesCollection($heroes);

foreach ($heroesCollection as $hero) {
    echo $hero->name . ' has ' . $hero->power . ' and uses a ' . $hero->weapon . "<br>";
}

// Prints:
// Superman has super strength and uses a heat vision
// Wonder Woman has superhuman strength and uses a lasso of truth
// Batman has genius-level intellect and uses a utility belt
```

## DocBlock

```php
/**
 * Class Hero
 * 
 * @param string $name The name of the hero
 * @param string $power The power of the hero
 * @param string $weapon The weapon of the hero
 */
class Hero {
    // ...
    public function __construct(protected $name, protected $power, protected $weapon) {}
}
```

_Docblock is a type of comment used in PHP to provide additional information about a function, class, or file. It is
written in a specific format and contains information such as the purpose of the code, parameters, return values, and
other notes. Docblocks are often used to generate documentation for a project._

## Exceptions

```php
// Exception is the base class for all Exceptions
// ErrorException is thrown when a error occurs at runtime
// ParseError is thrown when an error occurs while parsing
// TypeError is thrown when an argument is of wrong type
// ArgumentCountError is thrown when too few arguments are passed to a function
// ArithmeticError is thrown when an arithmetic operation fails
// DivisionByZeroError is thrown when a division by zero occurs
// AssertionError is thrown when an assertion fails
// ClosureThrowableError is thrown when an error occurs in a closure
// GeneratorThrowableError is thrown when an error occurs in a generator
// PDOException is thrown when an error occurs with a PDO operation
// SoapFault is thrown when an error occurs with a SOAP operation
// DOMException is thrown when an error occurs with a DOM operation
// IntlException is thrown when an error occurs with an internationalization operation
// ReflectionException is thrown when an error occurs with a reflection operation
// PHP_User_Deprecated is thrown when a deprecated feature is used
// PHP_User_Error is thrown when a user-defined error occurs
// PHP_User_Notice is thrown when a user-defined notice occurs
// PHP_User_Warning is thrown when a user-defined warning occurs
// JsonException is thrown when an error occurs with a JSON operation
```