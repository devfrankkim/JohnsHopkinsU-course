# Johns Hopkins University - Web Development
[Anchor tags](#Anchor-tags)


## Anchor tags 

- Internal linking to other pages in the site
- External linking to other web pages
- target="_blank" opens up for a separate tab
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
