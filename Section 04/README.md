# Section 03: Layouts: Floats, Flexbox, and CSS Grid Fundamentals

**About:** In this section, it is all about learning how to use CSS to build layouts using Floats, Flexbox, and Grids.

[Visit Site](https://bhoamikhona.github.io/html-css-bootcamp/Section%2004/index.html)
[Visit Challenge](https://bhoamikhona.github.io/html-css-bootcamp/Section%2004/challenge.html)

## Lessons Learned

- What is Layout?
  - Layout is the way text, images, and other content is placed and arranged on a webpage.
  - Layout gives the page a visual structure, into which we place our content.
  - Building Layout: Arranging page elements into a visual structure, instead of simply having them placed one after another.
  - There are 2 types of Layouts:
    - Page Layout: Laying out big pieces of content inside of a webpage
    - Component Layout: The bigger page layouts are made up of components, and these components need to have some kind of layout as they are made up of smaller pieces of content which also need to be arranged in some kind of way.
- Techniques of Building Layouts using CSS:
  - Floats
    - This is an old way of building layouts of all sizes, using the float CSS property. Still used but, getting outdated fast.
  - Flexbox
    - This is a modern way of laying out elements in a 1-dimensional row without using floats. It is perfect for component layouts.
  - Grid
    - This is another modern way of laying out elements in a full-fledged 2-dimensional grid. It is perfect for page layouts and complex components.
- Floats
  - `float: left` `float: right`
  - Floats are not a positioning scheme like absolute positioning but, they are still another way in which elements can be out of flow which is why it makes sense to compare it with absolute positioning.
  - What's different about floats is that floated elements do still have an impact on the surrounding elements i.e. text and inline elements will wrap around the floated element. This is why they are completely different than absolute positioned elements.
  - The container element to which float is applied, will not adjust its height to the element.
  - Collapsing Phenomena
  - Clearing Floats
    - `clear: both`
    - clearfix hack
- `box-sizing: border-box`
- Flexbox
  - `display: flex`
  - Horizontally, flex items will only take the amount of space that they need.
  - Vertically, flex items will take as much amount of space as the tallest flex-item.
  - `align-items: center` - this CSS rule, aligns all the flex items vertically centered.
  - `align-items: start` - this aligns all the flex items at the top (start) of the parent container.
  - `align-items: end` - this aligns all the flex items at the bottom (end) of the parent container.
  - `align-items: stretch` - this is the default value. i.e. all the flex items will take as much space as the tallest flex item vertically, and horizontally, they will only take space as needed.
  - To horizontally align the flex items in the parent container, we use a flex property called `justify-content`
  - `justify-content: center` - this will align all the flex items horizontally center in the parent container.
  - `justify-content: space-between` - this will distribute the remaining space in the parent container evenly in between flex items.
  - Flexbox is a set of related CSS properties for building 1-dimensional layouts.
  - The main idea behind flexbox is that empty space inside a container element can be automatically divided by its child elements.
  - Flexbox makes it easy to automatically align items to one another inside a parent contianer both, horizontally and vertically.
  - Flexbox solves common problems such as vertical centering and creating equal-height columns.
  - Flexbox is perfect for replacing floats, allowing us to write fewer and cleaner HTML codes.
  - **Flexbox Terminology**:
    - <ins>Flex Container</ins>: The element on which we want to use Flexbox is called the flex container. All we have to do in order to create a flex container is to set its `display` property to `flex`.
    - <ins>Flex Items</ins>: All the direct children of that flex container will become the so-called flex items.
    - <ins>Main Axis</ins>: The direction in which these flex items are laid out is called the main axis.
    - <ins>Cross Axis</ins>: The perpendicular axis to main axis is called the cross axis.
    - NOTE: We can change the direction of main axis and therefore also of the cross axis. We can also align elements along the main axis and along the cross axis in different ways.
  - Flex Container CSS Properties:
    - `gap: 0` (values: length) - To create space between items, without using margin.
    - `justify-content: flex-start` (values: flex-start, flex-end, center, space-between, space-around, space-evenly) - To align items along main axis (horizontally, by default)
    - `align-items: stretch` (values: stretch, flex-start, flex-end, center, baseline) - To align items along cross axis (vertically, by default)
    - `flex-direction: row` (values: row, row-reverse, column, column-reverse) - To define which is the main axis
    - `flex-wrap: nowrap` (values: nowrap, wrap, wrap-reverse) - To allow items to wrap into a new line if they are too large
    - `align-content: stretch` (values: stretch, flex-start, flex-end, center, space-between, space-around) - Only applies when there are multiple lines (flex-wrap: wrap)
  - Flex Items CSS Properties:
    - `align-self: auto` (values: auto, stretch, flex-start, flex-end, center, baseline) - To overwrite align-items for individual flex items.
    - `flex-grow: 0` (values: integer) - To allow an element to grow (0 means no, 1+ means yes)
      - `flex-grow` determines whether elements are allowed to grow as large as they can or not.
      - When `flex-grow` is set to `0` then all the flex-items would simply occupy the width that they need to fit their content.
      - When `flex-grow` is set to `1` then all the remaining space in the flex-container is evenly distributed by all the flex-items.
      - If you set `flex-grow: 1` to only one of the flex-items then only that item will take the available remaining space inside the flex-container. The rest of the items will only occupy the space needed horizontally.
      - Setting `flex-grow: 1` on all the flex-items here makes it so that they have the same size and it wouldn't even have to be 1. What matters is that they are the same number i.e. if all of them would be 5 then they would still have the same size.
      - If one of the flex-items is 2 then this flex-item would get double of the remaining space then these other ones.
      - NOTE: Setting one of the flex-items to `flex-grow: 2` and the rest to `flex-grow: 1` doesn't mean that the one with value 2 will get double the size. It means that it gets double of the available empty space than other flex items.
    - `flex-shrink: 1` (values: integer) - To allow an element to shrink (0 means no, 1+ means yes)
      - If there is not enough space in a container to fit the items with the size that we describe using `flex-basis` then the flexbox is allowed to shrink these items by default because flex-shrink is set to 1.
      - If want to change that, we simply need to set `flex-shrink` to `0`. But, in this case, the content will no loner fit inside the flex-container.
      - Therefore `flex-shrink: 0` is not advisable but, in some situations it is necessary.
      - To summarize, what `flex-shrink` does is to determine whether flexbox is allowed to shrink flex-items if necessary or not.
      - The opposite of `flex-shrink` is `flex-grow`.
    - `flex-basis: auto` (values: length) - To define an item's width, instead of the width property.
      - When we want to size flex-items and in particular with a width, then we usually do not use the width property. We use `flex-basis`.
      - `flex-basis` is not rigid, it is more like a recommendation that we make to the browser but, the browser will then based on the content, figure out the optimal length.
      - The reason for this is because, by default, flex-box is allowed to shrink elements so that they fit inside the flex-contianer. That is what `flex-shrink: 1` (default value) really means.
    - `flex: 0 1 auto` (values: int int int) - Recommended shorthand for flex-grow, flex-shrink, flex-basis.
    - `order: 0` (values: integer) - Controls order of items. -1 makes item first, 1 makes it last.
- CSS Grid
  - What is CSS Grid?
    - CSS Grid is a set of CSS properties for building 2-dimensional layouts.
    - The main idea behind CSS Grid is that we divide a container element into rows and columns that can be filled with its child elements.
    - In 2-dimensional contexts, CSS Grid allows us to write less nested HTML and easier-to-read CSS.
    - CSS Grid is not meant to replace flexbox. Instead, they work perfectly together. Need a 1D layout? Use Flexbox. Need a 2D layout? Use CSS Grid.
    - NOTE: The only way of defining space between the Grid items is `gap`. `margin` simply won't work.
  - CSS Grid Terminology:
    - <ins>Grid Container</ins>: The element on which we want to use Grid is called the grid container. All we have to do in order to create a grid container is to set its `display` property to `grid`.
    - <ins>Grid Items</ins>: All the direct children of that grid container will become the so-called grid items.
    - <ins>Row Axis</ins>: We cannot change the direction of Row Axis.
    - <ins>Column Axis</ins>: We cannot change the direction of Column Axis
    - <ins>Grid Lines</ins>: Grid lines divide the grids and separate the columns and rows.
    - <ins>Grid Cells</ins>: Intersection of Grid lines create grid cells. They need not always be filled.
    - <ins>Gutters/Gaps</ins>: Gutters/alleys/gaps are spacing between content tracks.
    - <ins>Grid Tracks</ins>: A grid track is the space between two adjacent grid lines i.e. it can be a row or a column.
  - Important Grid Container CSS Properties:
    - `grid-template-rows: rows: track size` and `grid-template-coluns: track size` - To establish the grid row and column tracks. One length unit for each track. Any unit can be used, new **fr** fills unused space.
    - `row-gap: 0 | length` and `column-gap: 0 | length` or combining both: `gap: 0 | length` - To create empty-space between tracks.
    - `justify-items: stretch |start | center | end` and `align-items: stretch | start | center | end` - To align items inside rows/columns horizontally/vertically
    - `justify-content: start | center | end | ...` and `align-items: start | center | end | ...` - To align items entire grid inside grid container. Only applies of container is larger than the grid.
  - Important Grid Items CSS Properties:
    - `grid-column: start line / end line | span number` and `grid-row: start line / end line | span number` - To place a grid item into a specific cell, based on line numbers. Span keyword can be used to span an item across more cells.
    - `justify-self: stretch | start | center | end` and `align-self: stretch | start | center | end` - To overwrite justify-items/align-items for single items.
  - Sizing Grid Columns and Rows
    - NOTE: `fr` stands for fraction.
    - `grid-template-columns: 2fr 2fr 1fr 1fr` - Creating grid columns of 2fr and 1fr unit size.
    - `grid-template-rows: 3fr 1fr` - Creating grid rows of 3fr and 2fr unit size.
    - Using `fr` instead of `px` will allow us to very easily create flexible columns and flexible rows. Using `px` allows us to give these tracks very rigid dimensions i.e. if you give a column a size of 200px, and if you resize the window, the size of the columns will always stay the same which is 200px and at some point it will even overflow the container. `fr` unit allows us to create flexible rows and columns which adapts to screen size change.
    - NOTE: At some point even 'fr' will overflow but, for the most part it will adapt to screen size change which `px` won't.
    - `grid-template-columns: 1fr 1fr 1fr auto` - In this case, the last column which has the value of `auto` will only take the necessary amount of space while the others will try to take 1/4 of the size of the space.
    - `grid-template-columns: 1fr 1fr 1fr 1fr` is equivalent to `grid-tempate-columns: repeat(4, 1fr)` - Here the the first parameter of repeat fuction is asking for how many times do you want to repeat, and the second parameter is asking for what do you want to repeat i.e. this is another way/easier way of saying "I need four of the 1fr columns".
  - **Explicit Grids**: We can define a fixed number of lines and tracks that form a grid by using the properties `grid-template-rows`, `grid-template-columns`, and `grid-template-areas`. These manually defined grid is called the explicit grid.
  - **Implicit Grids**: If there are more grid items than cells in the grid or when a grid item is placed outside of the explicit grid, the grid container automatically generates grid tracks by adding grid lines to the grid. The explicit grid together with these additional implicit tracks and lines forms the so called implicit grid.
  - Placing and Spanning Grid Items
    - `grid-column: 2 / 3`, `grid-row: 1 / 2` - this is will place the selected grid cell in row 1, column 2.
    - use the above propertied on grid-items.
    - `grid-row: 1 / 2` - this will extend the grid item up to 2 columns
    - `grid-row: 1 / -1` - This will extend the grid item all the way to the end
  - Aligning Grid Items and Tracks
    - Aligning grid items is a little bit different than it is in Flexbox because we can align both the tracks inside the container and we can also align the grid items inside of the tracks. This is because sometimes the grid items are smaller than the cells that they are in.
    - Aligning tracks inside containers: distribute empty space
      - `justify-content: center;`
      - `align-content: center;`
    - Aligning items inside cells: moving items around, inside cells
      - `align-items: center;`
      - `justify-content: center;`
      - Aligning a particular cell:
        - `align-self: end;`
        - `justify-self: end;`
- `display: none`

## Screenshots

![1](https://user-images.githubusercontent.com/50435319/225616986-444484ba-902c-4b91-b1bf-57a1f1782ca4.PNG)
![2](https://user-images.githubusercontent.com/50435319/225616993-8ae6c7a4-063c-43dc-a1f9-debe7a50f9aa.PNG)

## Authors

- [@bhoamikhona](https://github.com/bhoamikhona)
