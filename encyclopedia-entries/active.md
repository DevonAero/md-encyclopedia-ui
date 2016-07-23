# `:active`

*:active is a CSS pseudo-class*

The `:active` pseudo-class is commonly used with links (anchor tags) to change the appearance of the link when a user "clicks" on or activates it, letting the user know an action is about to happen.

The styles applied with this pseudo-class are only seen for a split second, otherwise you'll have to hold your left mouse button to see the style.


## Syntax

Introduction to the syntax/usage.

```
element:active {
		/* CSS rules in here */
}
```

### Values

This CSS pseudo-class doesn't have any values.

## Example 1

To understand how `:active` is used lets start with a simple example. 

In this example, we'll change the color of a link when a user clicks or (activates) it.

### HTML

``` 
<a href="http://www.youtube.com" class="btn">Go to YouTube!</a>

```

### CSS

```
.btn:active {

color: red;

}

```

## Example 3 - Complex

Lets take it up a notch and make it very apparent that a user has clicked on a link.

### HTML

```
<a href="http://www.reddit.com" class="annoying-btn">Head over to Reddit</a>
```

### CSS

```

.annoying-btn:active {
	font-size: 2em;
 	color: pink;
}

```



## Special Notes

### Usage

* Even though `:active` is used commonly with links. It can also be used with `<button>`s and other HTML elements.

### Bugs and Quirks

* `:active` styles can be overwritten by other pseudo-classes applied to a link so it's best to use it **after** you've specified your other styles.

