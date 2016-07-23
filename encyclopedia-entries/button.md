# `<button>`

*The HTML button element, the leader in user interaction*

This entry is to give you an overview on that exactly the HTML `<button>` is and how to use it.

## Syntax

Introduction to the syntax/usage.

```
<button name | type | value>
```

### Values

This is a CSS example, so each value would need it's own sub-section below.

#### name

The `name` attribute is used to name HTML elements. This helps submit information to server, like from forms. `name` can also be used to target elements with JavaScript or jQuery. Making it easy to modify those elements.

#### type

`type` determines which *type* of button you're about to use. Here's a list of commonly used `types`:

* `submit` - This submits your form to the server whenever this button is clicked.

* 

#### value

The `value` attribute is used to set a specific value on a button.

## Example 1

In this example we'll create a basic `<button>` to submit our form to our server.

```
  <form>
       <label for="fav-color">What is your favorite color?</br>
       <input type="text">
       <button type="submit">Submit Me!</button>
  </form>
```

Here, our `<button>` only uses one attribute `type` and its value is `submit`. As noted ealier when buttons are used to submit a form, that attribute and value is used.

## Example 3 - Complex

In a slightly more example, lets create a `<button>` that we can later use in JavaScript or jQuery to play and pause a video. 

```
HTML

    <button name="video-ctrl" value="play">
```

In our HTML we created a simple button with the `value` attribute and a  "show-btn" value (this could anything). We also added the `name` attribute so it'll be easy to target in JavaScript. Of course, we could also use a `class` or `id` attribute.

Consider this jQuery code:

```
jQuery

  $(function($) {
    var $ctrlBtn = $('[name=ctrl-btn]'),
        $videoPlayer = $('.video');

    if ($ctrlBtn.attr("value") === "play") {
      $videoPlayer.play();
    } else {
      $videoPlay.pause();
    }

  })(jQuery);

```

In this code, the video only places when the `<button>` element has a `value` of "play", if the value's anything else, the video will be paused.


## Special Notes

The basic `<button>` element is supported in all major browsers:

* Chrome
* Firefox
* Safari
* Opera
* Internet Explorer
* Microsoft Edge