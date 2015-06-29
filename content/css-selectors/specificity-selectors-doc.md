# Specificity on selectors.


```css
p.message {
  color: green;
}
#home #warning p.message {
  color: yellow;
}
#warning p.message {
  color: white;
}
body#home div#warning p.message {
  color: blue;
}
p {
  color: teal;
}
* body#home>div#warning p.message {
  color: red;
}
#warning p {
  color: black;
}
```

| Selector                                | Inline Style | IDs | Classes, Attributes, and Pseudo-classes | Element Types and Pseudo-elements |
| --------------------------------------- | ------------ | --- | --------------------------------------- | --------------------------------- |
| ```body#home div#warning p.message```   | 0            | 2   | 1                                       | 3                                 |
| ```* body#home>div#warning p.message``` | 0            | 2   | 1                                       | 3                                 |
| ```#home #warning p.message```          | 0            | 2   | 1                                       | 1                                 |
| ```#warning p.message```                | 0            | 1   | 1                                       | 1                                 |
| ```#warning p```                        | 0            | 1   | 0                                       | 1                                 |
| ```p.message```                         | 0            | 0   | 1                                       | 1                                 |
| ```p```                                 | 0            | 0   | 0                                       | 1                                 |

The results have been ordered according to specificity—the highest are at the top, and the lowest are at the bottom. As you 
can see, the top two selectors have exactly the same specificity, despite the extra universal selector and combinator in one 
of them. In this case, they tie for specificity and the one that appears last in the style sheet will be the winner. If you 
look at the original style sheet source above, the red color will be applied to the p element.

You can see from table that the selector p.message has a lower specificity than the selector #warning p. This is a common 
cause of head scratching among those new to CSS, who often think that a class selector will be specific enough to match an 
element in all cases.
