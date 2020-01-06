## Introduction to HTML

HTML stands for "HyperText Markup Language". It acts as the skeleton of a web page, providing the underlying structure. HTML does not define either decorative or functional qualities of your page (like colors or animations). Instead, it uses "elements" to build up a scaffold of what you can style and interact with using other languages.

HTML documents are composed of "elements". An element acts as a simple instruction to either display or prepare for a particular type of content. Some elements may be invisible and are used only for the benefit of your browser, while others display content, like text or images, on your web page.

Elements are composed of "tags". A tag is made up of an "opening bracket" (<), the name of the tag, and a closing bracket (>).

Most elements follow the structure of an "Opening tag", then "Content", then a "Closing tag". When following this format, we prefix the name of the closing tag with a '/' to indicate that we're closing an element.

Elements can stand by themselves or be "nested" within other elements. Nested elements have a "parent-child" relationship, meaning that we refer to the enclosing element as the "parent" and the nested element as the "child". We denote this nesting using indentation to make it easier for humans to read. Here are a few simple elements:
```
<p>My first element</p>
<section>
 <h3>
   I am the content of the "h3" element.
   The "h3" element is a "child" of the "section" element.
   The "section" element is the "parent" of the "h3" element.
   Notice how we indent to show these relationships.
 </h3>
</section>
```
Some elements don't require content or a closing tag. We call these "empty elements" or "void elements". Void elements don't accept content, which distinguishes them from typical elements.
```
 <img src="http://www.my.image.com" alt="My Cool image">
```
Web browsers implement what's called the Document Object Model as the basis for interpreting content (HTML, XML, SVG).

The [DOM](https://www.w3schools.com/js/js_htmldom.asp) is the interface we use to target elements and for watch for events.

Review some common elements

* p
* img
* a
* h1 ... h6
* span
* pre
* blockquote
* ul and ol

Review semantic elements (HTML5) (We refer to these new elements as "semantic" because they use plain English to communicate their purpose)

* header
* nav
* main
* article
* section
* aside
* footer

[Structural Semantics: The Importance Of HTML5 Sectioning Elements](https://www.smashingmagazine.com/2013/01/the-importance-of-sections/)

HTML elements often need data beyond their content. To supply this data, we can use "key-value" pairs inside the opening tag of the element. These pairs are referred to as attributes.
```
<a href="http://www.carolinacodeschool.org">Carolina Code School's Homepage</a>

<img src="red-panda.jpeg" alt="Adorable red panda cub laying in grass.">
```

https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes

## INTRODUCTION TO CSS

CSS has a history of mixed support across the major browser vendors, though there's now a well-known CSS standard (W3C) that most vendors try to follow.
https://www.w3.org/standards/techs/css#w3c_all

In web development, a polyfill is code that implements a feature on web browsers that do not support the feature.

[Can I Use?](https://caniuse.com/)

Browsers also apply what's referred to as a default style sheet that declares how elements should look when custom styles are not specified.

It's commonplace to include a stylesheet called a [CSS reset](http://html5doctor.com/html-5-reset-stylesheet/)

A modern, HTML5-ready alternative to CSS resets is [Normalize.css](https://necolas.github.io/normalize.css/)

A CSS rule is the actionable unit that CSS is written in and contains at least one selector (which specifies what the styles should be applied to) and one declaration (a statement made up of a property to target and a value to set that property to).

[CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

Using CSS

* External CSS File
* In a Style Block
```
<!-- It's possible to specify CSS styles in HTML files. These styles will only apply to elements in the document where they're declared, and will be baggage that comes along every time the page is retrieved.
Syntax is added to the head of your HTML document. -->

<style type='text/css'>
   a { color: blue; }
   #footer {
       bottom: 0px;
       width: 100%;
   }
</style>
```
* Inline with the Element
```
<p style="margin: 1%; font-size: 1.2em">Paragraph text</p>
```

Troubleshooting CSS
* semicolons at the end of all declarations
* browsers aren't consistent; just because something renders one way on your laptop doesn't mean it's going to look like that for everyone; use a CSS reset or normalize to make sure that most defaults will be consistent across browsers
* Remember that CSS assigns priority to selectors, called specificity. If a rule isn't being applied correctly, ensure that it's not being overwritten.

Selector Types
* Descendent combinators: #navigation li
* Child combinators: #container > p
* Adjacent sibling combinators: #container + li
  * will select only the specified element that immediately follows the former specified element
* General sibling combinators: p ~ img
 * will apply styles to any img elements following a p element
* Attribute combinators: input[type=text]
* Pseudo-class combinators (specific states elements can exist in): a:visited
  * https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes
* Pseudo-element combinators (lets you style specific part of the selected element): li::before
  * https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements
  * https://css-tricks.com/pseudo-element-roundup/

## THE COMMAND LINE

A Command Line Primer for Beginners
https://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything

* change directory: cd [<directory>]
* list: list the contents of a directory: ls [-a] [-l] [<directory>]
  * -a lists hidden files, -l outputs results in list format
* make directory: mkdir <directory>
* remove (delete a file or directory): rm <filename>, rm -rf <directory>
* use Mac's default program to open a file or folder: open <filename-or-directory>
* print working directory: Print the current directory: pwd
* copy (copy a file or directory to another directory): cp <filename> <directory-it-should-be-copied-to>, cp -R <directory> <directory-it-should-be-copied-to>
* open current working directory with Atom: atom .
* create a blank file if it doesn't exist: touch <filename>
* Run this command in Terminal.app to show hidden files in Finder: defaults write com.apple.finder AppleShowAllFiles YES

## RESOURCES

* HTML5 boilerplate: https://html5boilerplate.com/
* CSS properties: https://www.w3.org/TR/css-2018/#properties
* CSS properties that inherit (most popular): https://www.sitepoint.com/css-inheritance-introduction/
* CSS handbook: https://medium.freecodecamp.org/the-css-handbook-a-handy-guide-to-css-for-developers-b56695917d11

## Homework

* Command Line for Beginners
* Awesomely Ugly Website
* What was your first day of code school like? Was it what you expected? Was it scary? Was it fun? How do you feel about it? What did you learn?
