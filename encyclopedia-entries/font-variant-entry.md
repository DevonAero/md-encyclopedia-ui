# The `font-variant` Property
When small-caps is used, normal text is converted to uppercase. But difference is that small-caps letters are smaller than original uppercase letters. Check an example where I compare both uppercase and small-caps letters.

![](http://i.imgur.com/btPM1Su.png)

## Syntax
```
font-variant: normal | small-caps
```

## Values

#### inherit

Inherits the font-variant from parent

#### normal
The browser displays a normal font. This is default.

#### small-caps
The browser displays a small-caps font.  

When `small-caps` value is used, normal text will be displayed in uppercase, but it will be smaller than regular uppercase letters.


## Usage
It can be used to draw attention a new section of text, or to provide an additional style in a dictionary entry, if you decided to differentiate many parts typographically

```
example {
    font-variant: small-caps;
}
```
#### Difference between fonts:

![screen1](http://i.imgur.com/hVbHu7k.png)


#### Full HTML/CSS Example
![](http://i.imgur.com/4JPOYw5.png)

## Browser Support
---
The `font-variant` property is supported in all browsers (since IE6+, Firefox 2+, Chrome 1+ etc).  

| Chrome | Firefox | IE | Edge | Opera | Safari |
| :---: | :---: | :-----: | :---: | :---: | :-----: |
| yes | yes | yes | yes | yes | yes |
