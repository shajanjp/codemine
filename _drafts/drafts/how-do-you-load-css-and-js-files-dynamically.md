---
title: How do you load CSS and JS files dynamically 
categories: ["programming"] 
tags: ["JS"]
---
     You can create both link and script elements in the DOM and append them as child to head tag. Let's create a function to add script and style resources as below,
     ```javascript
     function loadAssets(filename, filetype) {
       if (filetype == "css") { // External CSS file
            var fileReference = document.createElement("link")
            fileReference.setAttribute("rel", "stylesheet");
            fileReference.setAttribute("type", "text/css");
            fileReference.setAttribute("href", filename);
       } else if (filetype == "js") { // External JavaScript file
            var fileReference = document.createElement('script');
            fileReference.setAttribute("type", "text/javascript");
            fileReference.setAttribute("src", filename);
       }
       if (typeof fileReference != "undefined")
            document.getElementsByTagName("head")[0].appendChild(fileReference)
      }
     ```

     **[⬆ Back to Top](#table-of-contents)**
