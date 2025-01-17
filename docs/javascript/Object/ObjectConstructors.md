---
tag: "javascript"
slug: "/javascript/object/object-constructors"
date: "2022-11-24"
title: Object Constructors
description: "The new Object() constructor creates an object wrapper for the given value."
category: "Advanced Javascript Object"
categoryOrder: 3
order: 1
githubPath: /javascript/Object/ObjectConstructors.md
contributor: [{ name: "Mahady Manana", link: "https://twitter.com/MahadyManana" }]
---

## Overview.

The `new Object()` constructor creates an object wrapper for the given value. If the value is null or undefined, it will create an empty object and return it. This object contains a set of key-value pairs that can be used to store and retrieve data.


```toc
# This code block will gets replaced with the TOC
# Don't worry if it shows in your editor preview
exclude: Table of Contents
tight: true
ordered: false
from-heading: 2
to-heading: 3
class-name: "table-of-contents"
```

## Syntax

The syntax for creating an object using the Object() constructor is as follows:

```javascript
new Object(value);
```

Parameter:
The value parameter is optional. If passed, it will be used as the initial value for the object. If not passed, an empty object will be created.

Examples:

```javascript
// Creating an empty object
const obj1 = new Object();
console.log(obj1); // {}

// Creating an object with an initial value
const obj2 = new Object({ name: "John", age: 30 });
console.log(obj2); // { name: 'John', age: 30 }
```

## Use cases with examples:

### Creating an object with dynamic keys:

```javascript
const key = "name";
const value = "John";

const obj = new Object();
obj[key] = value;

console.log(obj); // { name: 'John' }
```

### Using `new Object()` constructor to create a custom object:

```javascript
function Person(name, age) {
  this.name = name;
  this.age = age;
}

const john = new Person("John", 30);
console.log(john); // Person { name: 'John', age: 30 }
```

## Notes

- The `new Object()` constructor is not recommended for creating objects with predefined keys. Instead, you can create an [Object literal](/javascript/object/object-literals/) directly, like this:

```javascript
const obj = { name: "John", age: 30 };
```

- In modern JavaScript, it is more common to use class syntax to define custom objects. However, the `new Object()` constructor can still be used for creating basic objects or for compatibility with older code.

> <a href="https://github.com/mahady-manana/betatuto-docs/tree/main/docs/javascript/Object/ObjectConstructors.md}" target="_blank">Edit this page on Github</a>
