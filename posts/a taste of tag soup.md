TagSoup is a library to parse non compliant HTML.

To explain why you might want this, lets start by considering the following table.

```
<table id="test" border="1">
<tr>
<td>test
</tr>
</table>
```

Notice the missing closing <code>td</code> tag.

This still, in a browser renders as a table, border and all.

<a href="http://codekinder.com/wordpress/wp-content/uploads/2015/11/table.png"><img class="alignnone size-full wp-image-506" src="http://codekinder.com/wordpress/wp-content/uploads/2015/11/table.png" alt="table" width="62" height="60" /></a>
Though I don't have the actual stats, judging by how often I may mistakes in my own HTML, I think this I a valid enough reason to suspect the html you try to parse may not be compliant.

The problem is, a strict XML parser would not parse this. What we need is a parser which is lenient enough to parse malformed HTML with some degree of usefulness. Remote controlling a browser session would be a novel solution but it does incur a few overheads making it slower, harder to build and harder to code. Let's see how far we can get with some common xml parsers.

For example, using the popular HaXml the following error is produced when trying to parse the following source document.

```
Prelude Text.XML.HaXml.Parse>  xmlParse "" "<b>hello world</i></b>"                                                                                                                          
*** Exception: in element tag b,                                                                                                                                                                                   
tag <b> terminated by </i>                                                                                                                                                                                         
  at file   at line 1 col 15  
```

This library is way to strict to parse bad html. Let's try another. This time we will try the package known on hackage as simply <strong>xml</strong>

```
Prelude Text.XML.Light> parseXML "<b>hello world</i></b>"
[Elem                                                                                                                                                                                                              
   (Element{elName =                                                                                                                                                                                               
              QName{qName = "b", qURI = Nothing, qPrefix = Nothing},                                                                                                                                               
            elAttribs = [],                                                                                                                                                                                        
            elContent =                                                                                                                                                                                            
              [Text                                                                                                                                                                                                
                 (CData{cdVerbatim = CDataText, cdData = "hello world</i>",                                                                                                                                        
                        cdLine = Just 1})],                                                                                                                                                                        
            elLine = Just 1})]     
```

Slightly better, but as you can see the closing <code>i</code> tag is counted as text just like hello. 

Now, this time, we'll try using TagSoup.

What is Tagsoup? Tagsoup is a library for parsing and re-rendering html.

To get it,

```cabal install tagsoup```

After having done that. You can do some scraping. But first you might want to do some reading on the library by doing an online search for "tag soup haskell".

Also, if you do not know what "tag soup" is you might want to read up the page on wikipedia.

With that out of the way,

First import tagsoup
```
import Text.HTML.TagSoup
```

Now we can try and parse the broken HTML again.

```
Prelude Text.HTML.TagSoup> parseTags "<b>hello world</i></b>"
[TagOpen "b" [],TagText "hello world",TagClose "i",TagClose "b"]
```

...Now we're getting somewhere. 

As a small demonstration of the library, let's extract just the text from the html document.

```
Prelude Text.HTML.TagSoup> concatMap fromTagText $ filter isTagText $ parseTags "<b>hello world</i></b>"
"hello world"
```

So here you see a library which is capable of handling broken html documents in a fairly more malleable way than the usual xml library.
