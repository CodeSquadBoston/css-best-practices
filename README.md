# CodeSquad's CSS best practices

### Consistently indent styles within css rule blocks
Indenting the styles within a css rule makes it easy to tell which styles are within the rule and also make it easier to see where a rule starts and ends.  Make sure indent amounts are consistent across all your rules. 

#### Bad
Not indented at all
```css
.my-class {
background-color: red;
font-size: 20px;
}
```

Not indented a consistent amount
```css
.my-class {
  background-color: red;
    font-size: 20px;
}
```

#### Good
```css
.my-class {
  background-color: red;
  font-size: 20px;
}
```

### Each style gets its own line
Make sure each style within a rule gets its own line because it is hard to read all the styles within a rule block when they are jammed in one long line within a css rule.


#### Bad
Whole rule is on one line is defined on just one line.
```css
.my-class { background-color: red; font-size: 20px; }
```

Styles are all on one line.
```css
.my-class {
  background-color: red; font-size: 20px;
}
```
Not all styles have their own line.
```css
.my-class { background-color: red; 
  font-size: 20px; }
```

#### Good

```css
.my-class {
  background-color: red;
  font-size: 20px;
}
```


### Use dashes to separate words in class and id names
When naming classes and ids it helps to have a consistent naming convention for multi-word class names and the most common practice is to put a hypen between class and id names.


#### Bad
Camel case name
```css
.myClass {

}
```

underscore name
```css
#my_id {

}
```
#### Good
```css
.my-class {
  
}
```

### Use selectors over inline styles
Define styles using selectors instead of defining them directly in inline attributes because it is hard to apply styles across many items with inline styles and hard to update them if you make a small change.  More, inline styles are hard to override if you need to later.  The general best practice in css is to avoid them if at all possible.


#### Bad
Inline style
```html
<div style="background-color: red; font-size: 20px;">
```

#### Good
Inline style
```html
<div class="my-class">Good</div>
```
```css
.my-class {
  background-color: red;
  font-size: 20px;
}
```
