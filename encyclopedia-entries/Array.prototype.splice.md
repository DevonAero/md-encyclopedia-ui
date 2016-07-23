# `Array.prototype.splice()`

*`Array.prototype.splice()` is an `Array` method used to add or remove elements from an array.*

As noted earlier,  `Array.prototype.splice()` adds and/or removes elements from an array. After that process is finished an Array containing the deleted elements is returned by the method.

However, you can use it to alter an array without using it's return value.

## Syntax

Introduction to the syntax/usage.

```
Array.prototype.splice(startIndex, deleteCount, item1, item2...);
```

### Values

#### startIndex

`startIndex` is the position in the Array you want to start adding or removing elements.

Remember, Array elements are 0-based indexed. So to start from the first position you'd need to use `myArr[0]` instead of a `myArr[1]`.

#### deleteCount

`deleteCount` is the number of elements you want to remove from the array. 

If you wanted to remove 2 elements from an array, you'd pass the method a `2` like so: `Array.prototype.splice(startIndex, 2, item1...);`

You can also pass the method a `0` to only **add** elements and not remove them.

#### item1..item2.. and so on

These are the elements you want to add to the array you're working on. 

If you don't supply the method with these items (or elements), then `Array.prototype.splice()` will only remove items from the array.


## Example 1

Here's a basic example of how use `Array.prototype.splice()`.

Let's say we have an array of friends. We're all sitting about to play some video games, no scores have been posted yet, but you're number one and incredibly awesome so you want to be the first in the array.

Here's how to accomplish that:

```
  var friends = ["Josh", "Michael", "Kaleb", "Taylor", "Zack", "Jeff"];

  friends.splice(0, 0, "Devin");

  console.log(friends);
  
  // ["Devin", "Josh", "Michael", "Kaleb", "Taylor", "Zack", "Jeff"];
```
Sweet.

In this example, we're not using the return value from `Array.prototype.splice()`, we're just inserting an element into the first position of `friends`, (`friends[0]`);

## Example 2

Expanding on the first example, let's say at the end of your gaming session you want to poke fun at the losers of the games you played. But, you need to make an array of the losers first. 

*Assume this array is ordered by scores from greatest to least.*

```
var friends = ["Devin", "Josh", "Jeff", "Michael", "Kaleb", "Taylor", "Zack"],
    losers;

  losers = friends.splice(3, friends.length);

  console.log(losers);
  
  // ["Michael", "Kaleb", "Taylor", "Zack"]
```

This code starts at the third element in the array and deletes everything after it (from the `friends[3]` to the end of the array `friends.length`. 

Then, we store the results of `Array.prototype.splice()` in the variable called `losers` and we then print it to the console.

## Example 3 - Complex

Let's get a bit more advanced. While gaming, you found out one of your friends is using cheatcodes to boost his score and you all kick him out.

Now, you need to remove him from your `friends` array for more accurate scoring. The problem is you don't know what position in the array your cheating friend was at because one of the cheats he used randomize the array.

No problem, with our great knowledge of JavaScript, we can solve it.

```
  var friends = ["Josh", "Michael", "Taylor", "Jeff", "Devin", "Zack", "Kaleb"];

  friends.splice(friends.indexOf("Devin"), 1);

  console.log(friends);
  
  // ["Josh", "Michael", "Taylor", "Jeff", "Zack", "Kaleb"]

```

In this example, we're using another `Array` method called `Array.prototype.indexOf()` to search the `friends` array for for the string `"Devin"` and we use it as our starting index.

Since we only want to delete one element we pass the splice method a `1`.

Finally, we print our altered array of friends to the console. 

## Special Notes

Add information that you found that seemed lesser known. Common bugs, obscure bugs, important distinctions, all belong in this section.

