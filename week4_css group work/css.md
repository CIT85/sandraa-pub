# HTML
- Nesting an **image** in a **figure tag**
    - '< figure >
                            < img src="../img/caribbean.jpg" alt="Caribbean Beach"
                                title="I want to visit a castle by the Carribean Beach." width="400" height="225"
                                loading="lazy">
                            < figcaption >
                                Irish Carribean Beach Getaway
                            </ figcaption >
                        </ figure >'
---
# **CSS**
# What is cascading
> - Cascading is the code that styles web content.
- Example: HTML is the base of the house and CSS is the paint & furniture that adornes it
- Not a markup language it's a style sheets language, it can slectibvely style HTML elements
- Example: paragraph
- **Cascade** - think waterfall, style is read in the order it's entered so the last style is the one reflected.
### Note
> - Inline style- a way to add CSS to HTML without using a seperate file, its written inside of HTML tag using the style atttribute. Inline styles look and operate much like CSS, but they directly affect the tag they are written in, without the use of selectors.
---
## CSS Ruleset
- Ruleset: the whole structure, aka rule
1. **Selector**
- HTML element name at the start of the ruleset, it states what elements are to be styles (example < p >). 
### Note: p is the *selector*, color is the *property*, red is *property value*, and both property and red are the *declaration*

' p {
    color: red;
} '

2. **Declaration**
- A single rule of the properties that you want to style (example color:red;)
3. **Property Value**
- After the colon is the property value (example **property** : *property value*). In the example above there are many colors to choose from but only the color red was selected.

### **NOTES** see examples above
- { } apart from the sector each ruleset must be wrapped in curly braces
- : within each declaration, you must use the colon to sepereate the poperty from its value or values
- ; within each ruleset, you must use a semicolon to separate each declaration from the next one
- To modify multiple property values in one ruleset, write them separated by semicolons, like this: note each one starts a new line for clarity
' p{
    color: red;
    width: 500px;
    border: 1px solid black;
}'
---
## Selecting multiple elements ( element selectors )
>- You can also select multiple elements and apply a single ruleset to all of them. Separate multiple selectors by commas. Each one would be listed infront of the { } which then contains the ruleset within
' p,
li,
h1 {
  color: red;
} '
## Different types of selectors
- **Element selector** *(sometimes called a tag or type selector)* All HTML elements of the specified type.	p selects < p >
- **ID selector**	*The element on the page with the specified ID. On a given HTML page, each id value should be unique.*	#my-id
selects < p id="my-id"> or < a id="my-id">
- **Class selector**	*The element(s) on the page with the specified class. Multiple instances of the same class can appear on a page.*	.my-class
selects < p class=" my-class "> and < a class="my-class">
- **Attribute selector**	*The element(s) on the page with the specified attribute.*	img[ src ]
selects < img src=" my image. png "> but not < img >
- **Pseudo-class selector**	*The specified element(s), but only when in the specified state. (For example, when a cursor hovers over a link.)*	a:hover
selects < a >, but only when the mouse pointer is hovering over the link.
## Fonts and Text


---
# **Video Notes**
- ' < title >Document</ title > '
< link rel="stylesheet" href="main.css" >
- Other style sheet is applied but the one below overrides it, this one is external and the lower one is internal

   '< style > 
   p{
    color: limegreen;
   }

   </ style >'
   - *Style element is < style >*
   > See first few lines of w3_css index.html will display this play
   - Avoid inline CSS
   -'< body >
    < p style="color: blue">I'm learning CSS!</ p >
</ body >'
- this will over ride any other applied color since it is directly linked to the line and not overall document or bigger section
- external style sheet: does not mess with the HTML code since it's in it's own sheet
- 3 different ways to apply CSS on a HTML file code
1. Internal - in a style element; selector ex. p { }
2. External - another file and referencing it in
3. Inline - within a paragrph (try to avoid it)
---
## Why use ID?
- **Note** set up for the html file being used: html file -> h1 heading -> 3 articles -> each has its own h2 heading and paragraph inside
- **Chrome DevTools** right click on something on the screen and click Inspect
- Most common element selector = Body element, only one body element per page
1.  **Element selectors**: select all elements of that type, ex: p { } will affect all paragraphs (least specific)
2. **Class selectors**: these start with a period but can be named anything; classes can be used more than once. Classes are more specific that elements. Classes overrule the element that is overall; most common selector
3. **ID Selector**: more specific selector. ID's should only exist once in an html document, be unique. Not good practice to use inside of CSS. BEtter to use classes even element selectors (even more specific, but don't want to use)
- **Note** Can group selectors with a comma but without it turns into a nesting doll. example of nesting: h1 h2 
- Element within an Element: span within a paragraph element (lines 13-16) 
- Used instead of span in some cases, also clears up the code since span could be covering other things: '.highlight {
    text-transform: uppercase;
    background-color: gold;
}'
4. **CSS Universal Selector**
- Selects everything on the page is used to do a CSS reset (will be covered in the future). Example: '* { }. within the curly q's you would enter what you wanted to change between the curly's. That is not typically how you would use it, designated use will be later explained.
- **Specificity & Inheritance** 
- **Inheritance:** another element inherits the settings or properties of its parent elements, keeps us from rewriting code and keeps it clean
- body is a parent element, anything specified there will be inherited by the rest of the elements; things not related to those will not be inherited
- The border is included here but it's not specific inherited just over because of what it affets, the overall not a specific section: 'body{
    font-size: 22px;
    border: 3px solid black; 
}'
- This is selection no inheritance even though it looks like it: it depends on how it's written what it will affect '* {
    border: 1x solid red;
}'
- **Specifity** targets and affects a particular element
- Even though this is placed above the first paragraph it still affects its designated target since it has specificity and isn't general: '.gray {
    color:gray; }'
- Class is more specific than element selector so it over rules the element selector.
- **Note** use dev tools to see how css rules are being read, applied and read and overridden 

- **Dry** inheritance keeps code clean by not having to repeat code throughout, helps be more efficient.
- items for DRY can be placed in html, body or main. html overall code. body just in body. main just main.
- **!important & why you should not use it**
- over rides and ruins everything, its a clue that shows that the code is sloppy or un-organized. **DON'T USE**
- **specificity calculator** https://specificity.keegan.st/ resource
- Shows why and how each element, classes, attributes and ID's rank with one another
---
- **color & css** https://coolors.co/ resource
- Resource Coolrs, pick colors & copy the hexa. 
- Resource, WebAIM (Web accessibility in mind) another option BUT coolors is better
- **VSCODE color picker**
- Color- 140 available colors in html ( color wheel is available to help), usually set in the body
- Can use the table that pops up to view the # code as well as change color and transparancy when using rgba.
- **HSL:** hue saturation and lightness

- **Ways to specify color**
1. Background Example: ' background-color: blue; '
-  Background short hand Example: ' background: blue; '
2. Font Color Example: ' color: black; '
3. Color - another thing to find colors is RGB, example ' color: rgb(255,0,0) '
- Using RGB you select how much of each color you want, essentially you're mixing colors. Red, Green, Blue
- RGBA - red, green, blue, alpha. Alpha channel guides the transperancy
- RGB - 0-255, A - 0-1. 1 darkest and 0 is completely transparent
- Example: ' body {
    font-size: 22ps;
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.5;
    background: papayawhip;
    color: rgb(0,0,0);
}
p {
    color: rgba(0,0,0)
} '

- **Hexadecimal** - common way to specify decimals with the color pallet, works kind of like RGB and it has it's own way of coding its values 0-9/ a-f
- REd, Green, Blue: #RRGGBB; FF0000 = red, 00FF00 = Green, 0000FF = Blue
- *Can look at the visual studio options that pop up to see the hexadecimal codes*
- Shorthand' #000 " can be black instead of '#000000' because each pair matches; '#FFF' = white, #F00 = red, #0F0 = green, #00F= blue. Have to be pairs to use the short hand


- **Contrast Importance**
- Colors need to be readable and accessible 
- Coolors: use contrast checker here: Tools-> Contrast checker. It will grade your code contrast and let you know what the goals are
---
# **CSS** 4.8.24
## Video Notes 
- ' https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units ' Modzilla link

### Font Sizes 
- CSS units, units determine everything on the page
- **Most Common** :
- Values and Units
- Most common is pixles, only vlaue you will commonly use
- 1 pixle is common to 1/96th of an inch
- pixle = px
- **Checking the webpage**: three dots, settings, appearance
- Percentage: represents a fraction of some other value. Always reltive to another quantity, the parent. width percentage of the paragraph is relaventto the parent, Header.
- EXAMPLE: header is 100% then the child (width has up to 100%)
- 2 rut em (rem) , size is determeined by what is listed instead of defaults
- **character width - ch** The advance measure (width) of the glyph "0" of the element's font
- character width can help size columns
- *inspecting a page* lining the code. 3 dots on the right can help align 
- **VW & VH**
- *vw* - 1% of the viewport's width
- *vh* - 1% of the viewport's height
- *vw or % can be used for width but in some cases percentage might be better used for width*
- Issue Example: 'body {
    width: 100vw;} ' the issue with having 100vw is that the virticle content outgrows the page; doesn't account for scroll bar on the right it/ horrizonal. The bars appear when needed
- setting body to 100 it can be outgrown by content BUT setting min allows it to grow with the content
---
# **CHAPTER 5** #
**BOX MODEL OUTPUT ON DEVTOOLS**
- Center is content, padding, border, margin
- **Padding** - think of it as breathing room
- Margin - space left over surrounding the element
- **devTools** - inspect -> Element -> computed below, shows the map of unseen guidelines
- styles- 
- em responds to the font size font the element
- **Re-sizing** '*{ margin;0; padding: 0; box-sixing: content-box;} ', each one is specific to what they are named and doesn't affect any other field.
- Margin is on the outside of the css boxes that are created including elements syled
- Border, padding and content shown in devTools add up to the width placed in h1
- **Container Class**
- Container = a class; can be reference in / added to differen elements (header & main)

### **Margins** ###
- **Short & Long Hand for margin**
- *1 em is the same to the default font size*
- rem vs em: 
- Short hand: 'margin 1.5 em 2em 2em;' (applies to all margins instead of listing each one) 1.5em = top and bottom, 2em = right, 2em = left
- with short it can vary: two listed lengths is top & Bottom, left & right, but a vairation can be done: top & Bottom, left, right
- long hand: 'margin-top: 1.5em; margin-right: 2em; margin-bottom: 2em; margin-left: 2em;'
*Commenting Out CSS* shift + alt + a

### **Padding** ###
-  padding: 1.5em 2em 3em 4em;  same thing can be done short/long hand just like the margins

### **Borders**
- **Shorthand Border**
- 'border: 2px dashed red;'

### **Longhand Border** ###
    - 'border-top: 5px solid;
    border-right: 10px dotted;'  
    - COLOR can also be added here
    - 'border-top: 5px solid green;
    border-right: 10px dotted blue;'
    - '**border-top-style: 5px solid green;**
border-right-width: 10px dotted blue;
    **border-left-color: 5px blue;**'
    - WIDTH & STYLE can be added in the long hand after establishing border and side
    - Options to style the border: 'border: 2px outset red;' OR 'border: 2px double red;'OR 'border: 2px dashed red;'
### **OUTLINE**
- outline doesn't take up space like the border, set up is similar to border
    - 'outline: 5px solid purple;'
- **OUTLINE-OFFSET**
- offsets the outline (creates a space between the border and outline)
    - 'outline-offset: 5px'
- when px are done as negatives they are placed inside of the border
### **Circle** - **CIRCLE CLASS**
- Needs to be entered into the HTML to accessible in css' < /p>
< div class=""circle">< /div >
    </ main > '
- CSS CODE: '.circle {
    background-color: gold;
    width:100px;
    height: 100px;
    border: 2px solid #000;
    outline: 2px solid red;
    outline-offset: 0.25rem;
}'
- Complete Circle code: radius rounds it off to a circle
 .circle {
    margin: 3rem auto;
    background-color: gold;
    width: 100px;
    height: 100px;
    border: 2px solid #000;
    border-radius: 50px;
    outline: 2px solid red;
    outline-offset: 0.25rem;
}


- Ending Code for CH5 CSS
    - '*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.container {
    border: 10px double red;
    font-size: 1.5rem;
    margin: 1.5em;
   /*  margin-top: 1.5em;
    margin-right: 2em;
    margin-bottom: 2em;
    margin-left: 2em; */
    padding: 1.5em;
    outline: 5px solid purple;
    outline-offset: -20px;
}

.circle {
    margin: 3rem auto;
    background-color: gold;
    width: 100px;
    height: 100px;
    border: 2px solid #000;
    border-radius: 50px;
    outline: 2px solid red;
    outline-offset: 0.25rem;
}'
---
# **CHAPTER 6** #
**Typography** : different text declaration (decoration, transform,align, indent)
- *The way that text is arranged and presented*
- Control + B to shrink the tree
- font-size in body typically defaults to 16 px. 1 rem = 16px, 2 rem = 32 px
- text and font are two different things. 
    - *underline text* 'p {
    text-decoration: underline;
}'
    - *overline text*'p {
    text-decoration: overline;
}'
    - *strikethrough text*'p {
    text-decoration: underline;
}'
    - *default, anything else written is pushed back to default*'p {
    text-decoration: none;
}'
### **Transform**
- Changes the first letter of the word
- *Capital first letter* 'p {
    text-transform: capitalize;
}'
- *lowercase first letter* 'p {
    text-transform: lowercase;
}'
- *All uppercase letters* 'p {
    text-transform: lowercase;
}'

### **Align**
- aligns the text; default is left
- *Left* 'p {
    text-align: left;
}'
- *Jutify to square* 'p {
    text-align: left;
}'
- *right* 'p {
    text-align: right;
}'
### **Indentation**
- indent at the beginning, a tab'p {
    text-indent: 2em;
}'
>***THE FOLLOWING DON'T START WITH TEXT OR FONT***
### **IN LINE HEIGHT**
- Accepts units; accepts percent or numbers
- line spacing from one another, spacing between each line
- 'p {
    line-height: 1.5;
}'
### **LETTER-SPACING**
- seperates the letters, think wordsearch status
- 'p {
    letter-spacing: 1em;
}'
- .1 or something small when big it doesn't look readable

### **WORD SPACING**
- spaces out the words from one another
-'p {
    word-spacing: 1.5em
}'
- smaller number is better

### **LINE WEIGHT**
- how bold to make the letters
- ' p {
    font-weight: 300;
 }'
- Takes numbers but also words: light, normal, etc

### **FONT STYLE**
- from what I can tell its working with italics
- ' p {
    font-style: italic;
 }'
- takes words: italic, oblique, normal

### **FONT-FAMILY FALL BACK**
- different families that dicate the font throughout the page
- *Types of Generic families:* serif, sans-serif, monospace, cursive, fantasy
    - the serif's are the more common ones seen
    - monospace- gives each character equal spacing; looks like a typewriter
    - fantasy - heavy bold think sci fi
- Courier (full code) : 'font-family: 'Courier New', Courier, monospace;' (this type of code is called stacking)
    - it goes in order in the names listed for courier
    - name has quotes for spacing those that don't have won't use
- Arial (full code, stacking) - Arial, Helvetica, sans-serif
- Verdana (full code, stacking) - font-family: Verdana, Geneva, Tahoma, sans-serif
    - notice no quotes for this one
- Times New Roman (full code, stacking) - 'Times New Roman', Times, serif
- VS Code - suggests web safe fonts

### **GOOGLE FONTS** how to include them into your index and css files, using both the link and import methods.
- fonts.google.com
- search for fonts and can view the variation of styles for that font
- the number above the font states the weight of the font
- **To get the font** -> get font -> get code -> copy code and enter into the head in HTML
    - Once the HTML code is entered go back and look for the appropriate family-font line for css
        - HTML Code '    < link rel="preconnect" href="https://fonts.googleapis.com">
< link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
< link href="https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap" rel="stylesheet">'
        - CSS Code 'font-family: "Roboto", sans-serif;'

- *NOTE* the more fonts you use off of google the longer it will take for the page to load. Pick no more than necessary
- **LINK VS IMPORT**
- link is the long way and code needs to be entered in bot HTML and CSS
- import is short way and can be uploaded directly to CSS but can be entered into the head element in HTML
        - import code '@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap')'
        - Code above was embede into style element and can be placed within it in the head element

---
# **CHAPTER 7** #
### Style Links
- usually refers to an anchor tag
- 'a { }'
- 3 default styles
1. link are underlined and when not visited they are blue, once it's visited it turns purple
2. when hoveering over a link the mouse turns to a pointer courser
3. when clicking on the link it turns red, means its active

- *Underline*
     - CODE- 'a {
    text-decoration: underline;
}'
     - underline can be voided by replacing underline with none, BUT you still want to make the link stand out somehow
- *Cursor*
    - code to make it null - ' cursor:not-allowed;' (not something you want to do)
    - Default code -  'cursor: pointer;'
- *Color* 
    - can be set to different colors

    - Full Code -'a {
    text-decoration: none;
    cursor: pointer;
    color: blue;
}'
### Pseudo Class & how specificity and order works with links.
- *Psudeo Class* represent the current state of the element
      - the state of an anchor element can chage
      - it's either been visited or it hasn't
      - visited is more specific that the regular color element
      - Code 'body {
    padding: 10%;
    font-size: 2rem;
    font-family: 'Roboto', sans-serif;
}

a:visited {
    color: purple;
}

a {
    text-decoration: none;
    cursor: pointer;
    color: blue;
}



a:hover {
    color:dodgerblue;
}

a:active {
    color: red;
}'

- Can check reange/ level when it comes to specificity
- specificity.keegan.st
- though the more specific element is at the top that is not the way it should be laid out.
   - visited, hover, active all have same specificity so the order to them matters
   - if hover is over visited then hover won't work

   - Correct order:
   anchor tag -> visited -> hover ->active
   - focus- changes the color of the link when you tab through code 'a:hover, a:focus {
    color:dodgerblue;
}'
### psudeo class and how to use the color picker
- **make color works a bit better or how do not make it worst.**
- sometimes you don't take away the underline but make it all the same color, you would then keep the underline to make it stand out
- code 'a {
    color: hsl(207, 44%, 49%);
}'
- using the color wheel when you hover over the color click on the top and change the color format to HSL, copy and paste to another part and use that to get a similar color
- code 'a:hover, a:focus {
  /*   color:hsl(189, 44%, 49%); */
    opacity:0.9;
}'
- opacity changes everything 'main{
    opacity: 0.4
}' this makes everything lighter
- OR 'a:hover, a:focus {
    color:hsl(189, 44%, 49%, 0.8);
  /*   opacity:0.9; */
}'   GET transparancy 