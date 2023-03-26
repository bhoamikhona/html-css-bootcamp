# Section 08: Omnifood Project - Responsive Web Design

**About:** In this section, I continued building the Omnifood project and learned how to make it completely responsive. This means that the Omnifood website now adapts to various screen sizes.

[Visit Site](https://bhoamikhona.github.io/html-css-bootcamp/Section%2008/index.html)

## Lessons Learned

- Media Queries with `max-width`
- Breakpoints are the viewport at which we want our design to change i.e. breakpoints are pixel values that we want to put in our media queries
- Strategies for selecting Breakpoints
  - Based on screen-width ranges
    - Most mobile phones are in the range of 300px to 500px so a breakpoint of 600px would make sense
    - Similarly, most tablets are in the range of 600px to 900px so, the breakpoint for that could be 900px
    - landscape tablets are in the range of 900px to 1100px so, the breakpoint of 1200px makes sense.
    - and laptops & desktops would be larger than 1200px
  - Setting breakpoints at places where the design breaks down.
    - In this strategy, we completely ignore devices and device categories all together, and only look at our content and our design.
  - Combine both the stratgies mentioned above to make a flawless design flow through various screen sizes.
- Adding collapsed nav bar on smaller screen sizes

### HTML

- The meta tag below is crucial for responsive web design because, without this line of code, responsive design will not work on physical mobile devices. The reason for that is that browsers on mobile devices will basically zoom the page out by default until it fits the screen; and that is not what we want with media queries, we simply want to make our entire layout smaller i.e. less wide. This line of code will make it so that the page will match screen's width.
  - What `content="width=device-width` does is that it will set the width to be equal to device width and `initial-scale=1.0` will says that the initial scale should be 100% i.e. it will not zoom out of the page to fit it in the screen.
    `<meta name="viewport" content="width=device-width, initial-scale=1.0" />`

### CSS

- NOTE: `rem` and `em` do NOT depend on html font-size in media queries! Instead, we assume that, 1rem = 1em = 16px.
- `rem` -> root font-size
- `em` -> current font-size
- `rem` has some bugs in some browsers when used in media queries hence, we should use `em` instead of `rem` when using media queries.
- Selecting HTML elements using their attributes
  - e.g. `img[alt="Omnifood Logo"] { background-color: red; }`
- `pointer-events: none` - This property defines whether or not an element reacts to pointer events
- `visibility: hidden` - This property specifies whether or not an element is visible.
- [CSS Grid Layout: The `span` keyword](https://www.digitalocean.com/community/tutorials/css-css-grid-layout-span-keyword):
  - If you're placing items onto their parent grid with `grid-column` or `grid-row`, you can use the `span` keyword to avoid specifying end lines when items should span more than one column or row.
  - Given the following CSS rule for a grid item, which spans 3 columns and 2 rows:
  ```
  .item {
    grid-column: 2/5;
    grid-row: 1/3;
  }
  ```
  We can use the `span` keyword like this instead:
  ```
  .item {
    grid-column: 2 / span 3;
    grid-row: 1 / span 2;
  }
  ```
  - If you just say: `grid-column: span 2;` then all the columns in the grid would span across two columns i.e. they will take the space of two columns.

## Authors

- [@bhoamikhona](https://github.com/bhoamikhona)
