# Johns Hopkins University - Web Development
[Anchor tags](#Anchor-tags)


## Anchor tags 
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
