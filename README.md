# Johns Hopkins University - Web Development
*HTML*   
[Anchor tags](#Anchor-tags)    
[`&nbsp;`](#Non-breaking-space-(nbsp))    

 
****

*CSS*    
[Class Selector](#Selector)   
[Pseudo-Class Selectors](#Pseudo-Class-Selectors)


****

## HTML
### Anchor tags 
- Internal linking to other pages in the site
- External linking to other web pages
- target="_blank" opens up for a separate tab
- Linking to sections of a document
  
  "name vs id"
  - The document tree will look for "id"  first and then find "name"
 ```
    <a href="#section3">three</a>

    [id]
    <h2 id="section3">section3</h2>
    
    [name]
    <h2><a name="section3">section3</a></h2>
    <a name="section3"><h2>section3</h2></a>
 ```

### Non-breaking space (nbsp)

Place `&nbsp;` entity reference after the 1st word and after the 2nd word (with no spaces in between words and entity references) to keep the words together
```
frank&nbsp;is&nbsp;nice
```


****


## CSS

### Selector 

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
 /* Selects an unordered list that directly follows the element with ID title */

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
  =>  2, 3 ,4    
 /* Selects all Paragraphs that follow another paragraph until other tags show up*/       

ex)    
 p ~ p { color: red; }      
  => 2, 3, 4, 6, 9   
  /* Selects following Paragraphs except himself */        
 
ex)    
 div ~ p { color: red; }   


 ```
Note that 
in both the general sibling and adjacent sibling selectors the logic takes place 
within the same parent element.

That’s what siblings means.
Sharing the same parent. 
 ```



### Pseudo-Class Selectors
