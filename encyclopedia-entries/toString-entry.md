# Boolean.prototype.toString()

`Boolean` is a function creator, is used to create boolean primitives. Boolean(argument) returns a value of boolean type (not an object). 

```
var bool = Boolean(argument);
```

If the value of argument will be any of the falsey values, which are `NaN,0,false,undefined,null,"",` `bool` will be equal to `false` initially, otherwise it will be `true`. 

There is another preffered way of creating a boolean, by setting a variable to either true or false.

```
var bool = true;
```

Do not use a Boolean constructor to create a boolean, because in creates a boolean object instead, not a value of boolean type, here is an example:

```
var bool = new Boolean(argument); // This is a bad practice and not used in modern Javascript
```

So, let's create a primitive boolean value. Let's use a method `toString()` on it and see what happens:

![](http://i.imgur.com/XTL2nXk.png)

`bool.toString()` will return `"true"` - string representation of boolean primitive. That happens because `toString()` method is actually called on it's prototype which is Boolean.prototype. Let's check:

![](http://i.imgur.com/DZoggdi.png)


Primitives are not objects, but they do take methods from their prototypes. Basically, prototype is a storage for methods and shared properties. Every object and every prototype has a prototype, we can think of a succession of objects linked together to form a prototype chain. So `toString()` method is actually inherited via prototype chain from Object.prototype. I will explain it in detail.

Objects in Javascript can be organized into chains, so each property or method not found on one object will be taken automatically from another up to the chain. Major role here plays the special linking property called `__proto__` or in official documentation it will be `[[Prototype]]`. 

So what will be `__proto__` in our case when we assigned a variable to be true `var bool = true;`

![](http://i.imgur.com/YNZw5PB.png)

`bool.__proto__` is actually a `Boolean.prototype`, so they are linked together. When we go further and check how they are connected up the chain:

![](http://i.imgur.com/3moJ7c3.png)

And finally it should be clear now where `bool` is taking `toString()` method. It's actually on `Object.prototype`

![](http://i.imgur.com/bAWrSsL.png)


Full illustration of this:

![](http://i.imgur.com/hxKWv8d.png)


## Syntax

```
Boolean.prototype.toString()
```

## Usage

In the following code, `someBoolean.toString()` returns `"true"` - string representation of a value of boolean type:

```
var someBoolean = true;
var someVar = someBoolean.toString();
```  

## Browser Support
---

| Chrome | Firefox | IE | Edge | Opera | Safari |
| :---: | :---: | :-----: | :---: | :---: | :-----: |
| yes | yes | yes | yes | yes | yes |
