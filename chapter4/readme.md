# chapter 4 : Saving Time with Style Inheritance

* Here are examples of times when inheritance doesn’t strictly apply:
  * As a general rule,properties that affect the placement of elements on the page or the margins, background colors, and borders of elements aren’t inherited.
  * Web browsers use their own inherent styles to format various tags:Headings are big and bold, links are blue, and so on. When you define a font size for the text on a page and apply it to the <body> tag, headings still appear larger than paragraphs, and `<h1>` tags are still larger than `<h2>` tags. It’s the same when you apply a font color to the `<body>`; the links on the page still appear in good old-fashioned web-browser blue.
  * When styles conflict, the more specific style wins out. In other words, when you’ve specifically applied CSS properties to an element—like specifying the font size for an unordered list—and those properties conflict with any inherited properties—like a font-size set for the `<body>` tag—the browser uses the font size applied to the `<ul>` tag.
