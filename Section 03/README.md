# Section 03: CSS Fundamentals

**About:** This section is all about learning the basics of the second language of the web, that is, CSS. CSS is all about styling the content that we write in HTML. So, in this section, we will keep building our project and add some visual styles to it. We will also learn some theoretical concepts that are behind CSS so you understand how CSS works.

## Lessons Learned

### CSS

- What is CSS?
  - CSS stands for Cascading Style Sheets.
  - CSS is a core technology of the web, just like HTML.
  - CSS describes the visual style and presentation of the content written in HTML.
  - CSS consists of countless properties that developers use to format the content: properties about font, text, spacing, layout, etc.
  - A CSS rule is comprised of a selector and a declaration block.
    - A selector is any HTML element that you want to style.
    - A declration block consists a series of declarations. These declarations are nothing but a property and its value, and they are causually called styles.
  - In the end, our CSS code will be a lot of different CSS rules one after another where we select all of our elements and style them in any way we want.
- Inline CSS, Internal CSS, and External CSS
- Styling Text
  - color
  - font-size
  - font-family
  - text-transform
  - font-style
  - line-height
  - text-align
  - font-weight
  - letter-spacing
  - text-decoration
    - text-decoration shorthand: `text-decoration: underline dotted #ff4500` for `text-decoration-line`, `text-decoration-style`, and `text-decoration-color`
- NOTE: Just because the h1 is the main heading of the page, it doesn't mean that it also needs to be the biggest one. Being h1 is all about semantics, not only about what it looks like.
- Combining Selectors
  - List Selectors
  - Descendent Selectors
- Classes and ID Selectors
- Colors
  - RGB Model
    - e.g. `rgb(244, 179, 63)`
    - Every color can be represented by a combination of Red, Green, and Blue.
    - Each of the 3 base colors can take a value between 0 and 255, which leads to 16.8 million different colors.
  - RGB with Transparency ("alpha")
    - e.g. `rgba(244, 179, 63, 0.7)
  - Hexadecimal
    - Instead of using a scale from 0 to 255, we go from 0 to ff (255 in hexadecimal numbers)
    - Shorthand is used when all the colors are identical pairs.
      - e.g. `#2255ff` = `#25f`
    - When all three colors (Red, Green, Blue) are the same, we get a grey color. There are 256 pure greys to choose from.
  - Color Related CSS Properties:
    - color
    - background-color
    - border-color
- Borders
  - e.g. `border: 5px solid #1098ad` short hand for:
    - border-width
    - border-style
    - border-color
  - border-top, border-bottom, border-left, border-right
- Body Element Tag
- Pseudo Classes
  - `:first-child`
  - `:last-child`
  - `:nth-child()`
- Styling Hyperlinks using Pseudo Classes (in this order)
  - `a:link`
  - `a:visited`
  - `a:hover`
  - `a:active`
- Using Chrome Developer Tools
- Styling Lists
  - `list-style`
- Generic CSS Properties
  - `cursor: pointer`
  - padding and its shorthand
  - margin and its shorthand
- NOTE: Whenever you need some space inside of an element, which is very useful mostly when there is a background color, or a border on the element then you always used padding. On the other hand, in order to create some space outside of an element, or also to create space between multiple elements, always use margin. In case you need to add vertical space, it is a good practice to stick to margin-bottom.
- Global Reset
- Collapsing Margins: When we have two margins that occupy the same space, only one of them is actually visible on the page and that is usually the larger of the two.
- Adding Dimensions
  - CSS Units
    - px
    - %
- Centering WebPage
  - `margin: 0 auto`
- Positions:
  - Relative (Default): Elements are simply laid out according to their order in the HTML code.
  - Absolute: It allows us to absolutely position elements anywhere on the page.
- Pseudo-Elements: pseudo-elements are elements that don't exist in HTML but, that we can still select and style in CSS.
  - `::first-letter`
  - `::first-line`
  - `::after` - The `::after` pseudo element creates a pseudo element that will automatically be the very first child of the selected element. This is useful for some small cosmetic style for which we don't want to necessarily add a new element to HTML.
  - `::before` - This works the same as `::after`. The difference is that `::after` will become the very last child element of the one that we are selecting while `::before` will become the very first child element.
  - NOTE: By default any pseudo element is an inline element.
  - NOTE: the first property `content: ""` is mandatory. It can have something inside the quotes or it can be empty string.
- Adjacent Element Selector or Adjacent Sibling Selector
  - Sibling element is an element that is part of the same parent element.
  - The adjacent element is the sibling element that comes right after the one you are looking at.
  - e.g. to select paragraphs that come right after h3, this is how you select it: `h3 + p {color: red}`
- Negative Length

### CSS Theory

1. Conflicts Between Selectors

   - When multiple CSS rules apply to the exact same element, it is called conflicting selectors.
   - When this happens, all the CSS rules apply to that element.
   - When there are multiple declarations for the exact same element, then what matters are the selectors.

   - Highest to Lowest Priority for CSS Rules

     1. Declarations marked `!important`
        - Note: The important keyword is basically just a hack that you can use as the last resort to resolve conflicts in your CSS. But, this should usually not be used.
     2. Inline Styles
     3. Internal Styles
     4. ID (#) Selector
     5. Class (.) or Pseudo Class (:) Selector
     6. Element Selector
     7. Universal Selector

     - Note: When there more than one selector (e.g. more than one classes being applied to the same element, then the last selector in code applies.)

2. Inheritance and the Universal Selector

   - Inheritance

     - Inheritance is a mechanism by which some styles, i.e. some properties get their values inherited from parent elements to child elements.
       - Note: Not all properties get inherited. e.g. `border`
     - Inheritted styles are easily overriden whenever there is any rule that applies for the same property.
     - When we declare CSS rules in body, it does not apply to all the elements. Instead, they get passed down to all the chiled elements that are contained within the body.

   - Universal Selector
     - The Universal Selector simply selects every single element on the page and there is no inheritance involved.
     - This is useful if we want a certain property applied to all elements but, which does not get inherited.

3. The CSS Box Model

   - The box model defines how elements are displayed on a webpage and how they are sized.
   - In box model, each and every element on a webpage can be seen as a rectangular box, and each of these boxes can have content, a border, and space inside and outside of it.
   - Pieces of the Box Model:

     - Content: This is the actual content of the element. This could be text, images, table, video, or any other content that we might specify. Using CSS properties, we can specify both the height and the width of the content area.
     - Border: This is a line around the element, still inside of the element.
     - Padding: Padding is invisible space arount the content of the element. Just like the border, padding is also, still inside of the element i.e. padding is empty space that we can create inside of elements.
     - Margin: Margin is space outside of the element; between elements. In practice, we use margin in order to create space between elements on our page.
       - NOTE: All of these (i.e. content, border, padding, margin) are optional. We don't need to specify them. We can either mention all of them or some of them or none of them. It depends on how we want our layout to look like.
     - Fill Area: Area that gets filled with background color or background image. Remember that the text content and images are inside the content box but, the same does not apply for background images or the background color of an element. These properties will actually be applies not only to the content area but, to the entire fill area, which also includes the padding and the border. So, basically, if we apply a background color or image, it will occupy the entire visible part of the element.

   - How the box model calculates the size of an element based on content, border, and padding:
     - As mentioned before, we can specify the height and the width of the content area but, if we choose not to define them, then the box model will simply imply them based on the content.
     - However, the specified or implied heights and widths are actually not the final sizes of the element and this is because the border and the padding are also taken into account. So, the final width of an element, as we see it in the final alyout, is defined by the left border + left padding + spcified/implied width + right padding + right border; and same logic applies to the height of the element.
     - NOTE: Margin is not part of the width or height calculations of the elements since it is just a space around them.
     - This way of calculating heights and widths is actually just the default behavior of the box model but, we can change this default behavior.

4. Types of Boxes

   - There are different types of boxes in CSS.

   - Block Level Elements

     - These elements are formatted visually as blocks.
     - They occupy 100% of parent element's width, no matter the content.
     - They are stacked vertically by default, one after another.
     - By default, most of the HTML elements are block level elements. e.g. body, main, header, footer, section, nav, aside, div, headings, paragraphs, lists, etc.
     - `display: block`

   - Inline Elements

     - Inline elements only occupy the space necessary for its content.
     - They cause no line-breaks after or before the element.
     - Box model applies in a different way: heights and widths do not apply.
     - Paddings and margins are applied only horizontally (left and right), not vertically.
     - e.g. anchors, strong, em, button, etc
     - `display: inline`

   - Inline-Block

     - Inline-block elements look like inline elements from outside but, they behave like block elements on the inside.
     - They occupy only necessary amount of space and do not cause a line-break.
     - The box model applies as it does on block elements i.e. we can set height, width, margin, and padding as we would on a block element.
     - e.g. images
     - `display: inline-block`

- Note: We can change an element from Inline to Block and vice versa. We can do this by using `display` CSS property.

5. Absolute Positioning
   - `position: absolute`
   - Absolute positioning allows us to absolutely position elements anywhere on the page.
   - Element is removed from the "normal flow" i.e. Relative Positioning.
   - The element on which the absolute positioning is applied to, completely loses any impact on surrounding elements, and, in-fact, it might even overlap them.

### Developer Skills

1. Googling and Reading Documentation
   - Stackoverflow
   - MDN Docs
   - W3 Schools (Not Recommended)
2. Debugging and Asking Questions
   - [Markup Validation Service](https://validator.w3.org/)
   - [Diff Checker](https://www.diffchecker.com/)
   - A rule of thumb: Besides the rules that we already learned before about selector priority, if one selector is way more complex than the other, then many times, it is the more complex one that gets applied. Therefore, avoid writing complex selectors.

### More HTML

- `<link>`
  - The link tag defines the relationship between the current document and an external resoure.
  - It is most often used to link to external style sheets or to add a favicon to your website.
  - It is an empty element, it contains attributes only.
  - In order to actually position the element that is absolutely positioned, we can use the `top`, `bottom`, `left`, or `right` properties to offset the element from its <ins>relatively</ins> positioned container.
- [HTML Emoji Entities](https://www.htmlsymbols.xyz/):
  - Heart Symbol: `&#10084`;
  - Heart Stars: `	&#x1F496;`

## Authors

- [@bhoamikhona](https://github.com/bhoamikhona)
