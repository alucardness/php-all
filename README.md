# PHP ✨Magic ✨

## _All in One_

Table of contents.

- [How to install PHP](#how-to-install-php)
- [Print variables](#how-to-print-variables)

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