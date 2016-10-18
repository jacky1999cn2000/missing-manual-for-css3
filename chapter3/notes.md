# chapter 3

* descendants of a tag
```
  li a
```  
this will select all <a> tags that are descendants of <li> tag, not has to be direct descendants; so it can select `<li><a><a/></li>`, as well as `<li><strong><em><a><a/></em></strong></li>`

* Pseudo-Classes and Pseudo-Elements
  * Styles for Links
    * a:link
    * a:visited
    * a:hover (can apply to other tags or class, e.g. `tag:hover` or `.class:hover`)
    * a:active
  * More Pseudo-Classes and Pseudo-Elements
    * :focus (`input:focus { background-color: #FFFFCC; }`)
    * :before and :after (https://css-tricks.com/almanac/selectors/a/after-and-before/)
    * ::selection

* Attribute Selectors
  * With attribute selectors, you can single out tags that have a particular property. For example, here’s how to select all <img> tags with a title attribute:`img[title]`
  * with class `.photo[title] `
  * with attribute value
  ```
    a[href="http://www.cafesoylentgreen.com"]{
      color: green;
      font-weight: bold;
    }
  ```
  * with regex `a[href^="http://"]` `a[href$=".pdf"]` `img[src*="headshot"]`

* Child Selectors
  * Unlike a descendant selector, which applies to all descendants of a tag (children, grandchildren, and so on), the child selector lets you specify which child of which parent you mean. e.g. `body > h2`
  * CSS also includes some very specific pseudo-classes for selecting child elements. They let you fine-tune your selectors for many di erent arrangements of HTML.
    * :first-child pseudo-element lets you select and format just the first of however many children an element may have.
    * `h1:first-child` This selector applies to *any <h1> tag that is a first child*.
    * `li:last-child li:nth-child li:nth-child(odd) li:nth-child(even) li:nth-child(2) li:nth-child(3n) li:nth-child(3n+2)`
    * `p:only-child`

* Child Type Selectors
  * `.sidebar p:first-of-type`
  * `.sidebar p:last-of-type`
  * ` img:nth-of-type(odd) { float: left; } img:nth-of-type(even) { float: right; }`

* Siblings
  * A tag that appears immediately after another tag in HTML is called an adjacent sibling. The adjacent sibling selector uses a plus sign (+) to join one element to the next. So to select every paragraph following each <h2> tag, use this selector: h2 + p (spaces are optional, so h2+p works as well). The last element in the selector (p, in this case) is what gets the formatting, but only when it’s directly after its brother <h2>.
  * There’s another sibling selector called the general sibling combinatory selector (say that three times fast). It’s simply a ~ (tilde) and it means “select all siblings of this type.” For example, while h2 + p selects a single <p> tag that immediately follows an <h2> tag, h2 ~ p selects all <p> tags that are siblings (that is, on the same level) of the h2. To be honest, you may never find a good use for this selector, but CSS is nothing if not thorough.

* The :target Selector
  ```
    <button>
      <a href="#signupForm">Sign up for our newsletter</a>
    </button>
    <form id="signupForm">
      <label for="email">What's your email address?</label>
      <input type="email" id="email">
      <input class="btn" type="submit" value="Sign up">
    </form>
  ```
  ```
    #signupForm {
      display: none;
    }
    #signupForm:target {
      display: block;
    }
  ```

  * The :not() Selector
    * `p:not(.classy) { color: blue; }   a[href^="http://"]:not([href^="http://mysite.com"])  a[href^="http://"]:not([href*="mysite.com"])`
    * limitations
      * •You can only use simple selectors with the:not()selector.In other words you can use element selectors (like html or p), the universal selector (* [see page 49]), classes (.footer, for example), IDs (#banner, for example), or pseudo-classes (:hover, :checked, :first-child, and so on). So the following are all valid:
      ```
        .footnote:not(div)
        img:not(.portrait)
        div:not(#banner)
        li:not(:first-child)
      ```
      * You can’t use descendant selectors(like div p a,pseudo-elements(like::first- line), group selectors, or combinators (like the adjacent sibling selector h2 + p).
      * you can only use :not() once with a selector.
