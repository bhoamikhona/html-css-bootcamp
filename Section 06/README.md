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
  - Hero Section
  - Footer
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

### HTML

- `<blockquote>` - The blockquote tag specifies a section that is quoted from another source. Browsers usually indent blockquote elements.
- `&nbsp;` - Non-breaking space entity which is a space that will not break into a new line. This is handy when breaking the words might be disruptive. Another common use of the non-breaking space is to prevent browsers from truncating spaces in HTML pages.

## Authors

- [@bhoamikhona](https://github.com/bhoamikhona)
