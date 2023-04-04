# PHP ✨Magic ✨

## _All in One_

Table of contents.

- [How to install PHP](#how-to-install-php)
- [Print Variables](#how-to-print-variables)
- [Constants](#constants)
- [Magic Constants](#magic-constants)
- [Data Types](#data-types)

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