# Section 05: Components and Layout Patterns

**About:** In this section, we will take a look at common website components and also common layout patterns. So, things like sliders, testimonials, pricing tables, navigations, the Z patterns, and many more. This is important because being able to choose between some well-established patterns and components will allow you to design and build your own pages in the future with way more confidence. Now, besides just learning about these common patterns, we will also build some of them in this section using code.

## Lessons Learned

### Design & Layout

- Elements and Components
  - Elements => Components => Layouts using Patterns => Webpages
  - Use common elements and components to convey your website's information.
  - Combine components into layouts using common layout patterns.
  - Assemble different layout areas into a complete, final page.
- Common Elements:
  - Text
  - Buttons
  - Images
  - Input Elements
  - Tags
- Common Components
  - Breadcrumbs
  - Pagination
  - Alert and Status Bars
  - Statistics
  - Gallery
  - Feature Box
  - Preview and Profile Cards
  - Accordion
  - Tabs
  - Carousel
  - Customer Testimonials
  - Customer Logos
  - Featured-in Logos
  - Steps
  - Forms
  - Tables
  - Pricing Tables
  - Modal Windows
- Common Section Components
  - Navigation
    - Sub-Menus & Complex Sub-Menus
    - Secondary Navigation
  - Hero Section
  - Footer
    - Site Map
  - Call-to-Action Section
  - Feature Row
- Common Layout Patterns
  - Row of boxes or cards
  - Grid of boxes or cards
  - Z-pattern
  - F-pattern
  - Single column
  - Sidebar
  - Multi-column/Magazine
  - Asymmetry/Experimental

### CSS

- With `flex-direction` set to `column`:
  - `algin-items` aligns items horizontally, not vertically.
  - `justify-content` aligns items vertically, not horizontally.
  - `gap` acts like `margin-bottom`, not `margin-right`
- `transform: scale(1.5)` - The transform property applies a 2D or 3D tranformation to an element. This property allows you to rotate, scale, move, skew, etc., elements.
- `scale()` - The scale function defines a transformation that resizes an element on the 2D plane. Since the amount of scaling is defined by a vector, it can resize the horizontal and vertical dimensions at different scales.
- `translate()` - The translate function repositions an element in the horizontal and/or vertical directions.
- `border-collapse: collapse` - The border-collapse property sets whether table border should collapse into a single border or be separated as in standard HTML.
- NOTE: When it comes to table, only sizing the first row (heading row) in terms of width will suffice since the rest of the rows will follow according to it.
- `background` - The background property is a shorthand property for:

  - `background-color`
  - `background-image`
  - `background-position`
  - `background-size`
  - `background-repeat`
  - `background-origin`
  - `background-clip`
  - `background-attachment`
  - It does not matter if one of the values above are missing, e.g. `background: #ff0000 url("smiley.gif");` is allowed.

- Building and Using Utility Classes
- CSS Units:

  - `vh` - Viewport Height
  - `vw` - Viewport Width

- `background-image: url("image/url")` - The background-image property sets one or more background images for an element. By default, a background-image is placed at the top-left corner of an element, and repeated both vertically and horizontally.
- `background-size: cover` - The background-size property specifies the size of the background images. The value of cover resizes the background image to cover the entire containe, even if it has to stretch the image or cut a little bit off one of the edges.
- `background-image: linear-gradient(red, yellow, blue)` - The linear-gradient() function sets a linear gradient as the background image.

- `overflow: scroll` - The overflow property controls what happens to content that is too big to fit into an area.
  - It specifies whether to clip the content or to add scrollbars when the content of an element is too big to fit in the specified area.
  - The `overflow` property has the following values:
    - `visible` - Default. The overflow is not clipped. The content renders outside the element's box.
    - `hidden` - The overflow is clipped, and the rest of the content will be invisible.
    - `scroll` - The overflow is clipped, and a scrollbar is added to see the rest of the content.
    - `auto` - Similar to `scroll` but, it adds scrollbars only when necessary.
  - NOTE: The `overflow` property only works for block elements with a specified height.
- NOTE: When using flexbox, the flex items will shrink if `overflow: scroll` is applied. This is because the the flex-items are set to `flex-shrink: 0` by default and so, the scroll bar won't show if they shrink and fit within the container. In order to fix that, simply set `flex-shrink: 0` along with setting `overflow: scroll` and it should work.

### HTML

- `<blockquote>` - The blockquote tag specifies a section that is quoted from another source. Browsers usually indent blockquote elements.
- `&nbsp;` - Non-breaking space entity which is a space that will not break into a new line. This is handy when breaking the words might be disruptive. Another common use of the non-breaking space is to prevent browsers from truncating spaces in HTML pages.
- `<header>` - The header element represents a container for introductory content or a set of navigational links. A header element typically contains one or mor headings, logo or icon, and authorship information. You can have several header elements in one HTML document. However, header cannot be placed within footer, address, or another header element.
- `<menu>` The menu tag defines a list/menu of commands. It is used to context menus, toolbars, and for listing form controls, and commands.

| `<nav></nav>`                                                                                                                      | `<menu></menu>`                                                                          |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| The nav tag creates navigation block which provides link for contents either on the same document/page or any other document/page. | The menu tag creates a list or menu of commands which can be utilized by the users.      |
| The nav tag is specifically for grouping elements in a Website.                                                                    | The menu tag is for web applications to handle/design interactive elements.              |
| The contents of nav tag are `<a href="#">`, `<ul>`, `<ol>`, and `<li>` etc.                                                        | The contents of menu tag are `<menu>`, `<menuitem>`, `<li>`, `<hr>`, and `<script>` etc. |

## Screenshots

### 01 Accordion

![1](https://user-images.githubusercontent.com/50435319/225615063-1be7de0f-b13f-40fd-ac01-4f12330fd9a2.PNG)

### 02 Carousel

![2](https://user-images.githubusercontent.com/50435319/225615068-e9306118-2ffd-4ec2-b455-2e9101e1a458.PNG)

### 03 Table

![3](https://user-images.githubusercontent.com/50435319/225615071-2158d83f-f579-48bd-a162-8fe73f984017.png)

### 04 Pagination

![4](https://user-images.githubusercontent.com/50435319/225615073-13b545e1-7115-4935-b74b-a70021a07ebd.png)

### 05 Hero Section

![5](https://user-images.githubusercontent.com/50435319/225615075-36e0ae22-29c7-4d13-853a-d4aa0443e582.png)

### 06 App Layout

![6](https://user-images.githubusercontent.com/50435319/225615058-8447360b-e3cc-4d5a-965b-f42669b987dc.PNG)

## Authors

- [@bhoamikhona](https://github.com/bhoamikhona)
