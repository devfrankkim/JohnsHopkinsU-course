# Johns Hopkins University - Web Development

_HTML_  
[Anchor tags](#Anchor-tags)  
[`&nbsp;`](#Non-breaking-space)

---

_CSS_  
[Class Selector](#Selector)  
[Pseudo-Class Selectors](#Pseudo-Class-Selectors)  
[Specificity](#Specificity)  
[Box-sizing:border-box](#Border-box)  
[Margin-collapse](#Margin-collapse)  
[Content overflow](#Content-overflow)  
[Floats](#Floats)  
[Positioning](#Positioning)

---

## `HTML`

## Anchor tags

- Internal linking to other pages in the site
- External linking to other web pages
- target="\_blank" opens up for a separate tab
- Linking to sections of a document

  "name vs id"

  - The document tree will look for "id" first and then find "name"

```
   <a href="#section3">three</a>

   [id]
   <h2 id="section3">section3</h2>

   [name]
   <h2><a name="section3">section3</a></h2>
   <a name="section3"><h2>section3</h2></a>
```

## Non-breaking space

Place `&nbsp;` entity reference after the 1st word and after the 2nd word (with no spaces in between words and entity references) to keep the words together

```
frank&nbsp;is&nbsp;nice
```

---

## `CSS`

## Selector

```
Combining Selectors
```

- Element with class selector (selector.cass)
- Child(DIRECT) selector(selector > selector) -> You can't miss parents
- Descendent selector (selecetor selector)
- Adjacent sibling selector (selector + selector)
- General sibling selector (selector ~ selector)

```
"+"
An adjacent sibling combinator selector
allows you to select an element that is directly after another specific element.
```

```
"~"
General sibling selector
is very similar to the adjacent sibling combinator selector.

The difference is
adjacent sibling selector skips himself.
BUT General sibling selector only skips first element
```

ex)  
#title + ul { margin-top: 0; }  
 /_ Selects an unordered list that directly follows the element with ID title _/

```
  <body>
   <div>
      <p>1</p>
      <p>2</p>
      <p>3</p>
      <p>4</p>
      <div>
        <p>5</p>
      </div>
      <p>6</p>
      <div>7</div>
      <div>
         <p>8</p>
      </div>
      <p>9</p>
    </div>
  </body>
```

ex)  
 p + p { color: red; }  
 => 2, 3 ,4  
 /_ Selects all Paragraphs that follow another paragraph until other tags show up_/

ex)  
 p ~ p { color: red; }  
 => 2, 3, 4, 6, 9  
 /_ Selects following Paragraphs except himself _/

ex)  
 div ~ p { color: red; }

```
Note that
in both the general sibling and adjacent sibling selectors the logic takes place
within the same parent element.

That’s what siblings means.
Sharing the same parent.
```

## Pseudo-Class Selectors

Many pseudo-class selectors exist

- :link
- :visited
- :hover
- :active
- :nth-child(....)  
   ex) a:hover div:nth-child(10) {
  color: red;
  }

## Specificity

- Highest score wins
- !important -> Have to be careful

1. style="..."
2. ID
3. Class, pseudo-class, attribute
4. #of elements

ex)

[style | ID | Class | elements]

1. div #winner { color: blue; }  
   -> 0 1 0 1
2. div .big p { color: green; }  
   -> 0 0 1 2

#myColor {color: green;} -> winner

.myColor {color: blue;} -> id before class

## Border-box

- content-box is default
- { box-sizing: border-box; }
- Everything is playing inside the width you set
- The \* (universal) selector

## Margin-collapse

- Collapsing for Vertical margins
- Larger margin wins
- Horizontal margins combine together

## Content overflow

- overflow: hidden -> hiding flowing content
- overflow: auto -> scroll bar
- overflow: scroll -> both ways

## Floats

- Floating elements can produce very flexible layouts
- Floats are taken out of normal document flow
- Floats don't have vertical margin collapse
- To use normal document flow, use the "clear" property(right, left, both)

## Positioning

- "From" top, right, bottom, left
- Has negative values
- positons always look for ancestors

### Static Positioning

- normal document flow.
- Default for all elements, except HTML(relative)

### Relative Positioning

- Element is positioned relative to its position in normal document flow
- HTML(by default)
- The children will move together with the parent(relative)

### Absolute Positioning

- All offesets(t,r,b,l) are relative to the position of the nearest ancestor which has positioning set on it, other than static

- By default, html is the only element that has non-static positioning set on it(relative)

- Needs a relative OR absoulte parent or ancestor (check the parent's position first)

- It bubbles up to HTML(relative by default) and check the positioning
