#Modern (Sans) Theme for IAWriter with Syntax Highlighting for Code Blocks

![screenshot](/screenshot.png)

* This is a modified version of the orginal Modern (Sans) Theme by [IAwriter](https://ia.net/writer) 
* Code Blocks are highlighted with [highlight.js](https://highlightjs.org/)
* Learn more about custom templates for IAWriter [here](https://github.com/iainc/iA-Writer-Templates) 

##Usage
* Drag an drop the 'sansWithHLJS.iatemplate' file into Preferences => Templates.

##Modifications

**sansWithHLJS.iatemplate.iatemplate/Contents/Resources/document.html**
```html

<!doctype html>
<html>
<head>
    <meta charset="UTF-8">
    <link rel="stylesheet" media="all" href="normalize.css">
    <link rel="stylesheet" media="all" href="core.css">
    <link rel="stylesheet" media="all" href="style.css">
    <link rel="stylesheet" href="hljs_styles/monokai-sublime.css"> <!--Change Theme here-->
    <script src="highlight.pack.js"></script>
    <script>

        document.addEventListener("DOMContentLoaded", function(){
            document.body.addEventListener('ia-writer-change', function(event) {
                var codeBlocks = document.querySelectorAll('pre code');
                [].forEach.call(codeBlocks, function(codeBlock) {
                    hljs.highlightBlock(codeBlock);
                });
            });
        });

    </script>
</head>
<body data-document>&nbsp;</body>
</html>

```


**sansWithHLJS.iatemplate/Contents/Resources/core.css**
```css

pre {
  padding: 1rem;
  overflow: hidden;
  background-color: #23241f;/*HLJS Theme Overwrite;*/
}

pre code {
  padding: 0;
  border: transparent; /*HLJS Theme Overwrite;*/
}

```

