# Section 09: Omnifood Project - Effects, Optimizations, and Deployment

**About:** This section is all about finishing the Omnifood project by tying up some loose ends. Adding javascript to make the mobile navigation work, compress images for better performance, adding some finishing touches, and deploying it to the internet.

[Click Here to visit the Website](https://omnifood-bhoami.netlify.app/)

## Lessons Learned

- Short Introduction to Javascript
- Implement Javascript to make mobile navigation work
- Smooth Scrolling
- Sticky navigation bar
- Testing on various browsers
- Lighthouse testing
- Adding Favicon and Meta Description
- Image Optimizations
- Deploying to Netlify
- Making the form work with Netlify forms

### Javascript

- `defer` keyword - The defer attribute is a boolean attribute. If it is set, it specifies that the script is downloaded in parallel to parsing the page, and executed after the page has finished parsing. It is only used for external scripts (should only be used if the `src` attribute is present).
- `console.log("Hello, World!")` - This method writes (logs) a message to the console.
- `const` keyword - const defines a variable in Javascript and it cannot be reassigned. const variables must be assigned a value when they are declared.
- Selecting and changing HTML elements and their styles using JS.
- `addEventListener()` - This function attaches an event handler to an element.
- webkit prefixes

### HTML

- page anchors using id selectors
- `<picture>` - The picture tag gives web developers more flexibility in specifying image resources. The most common use of the picture element will be for art direction in responsive designs. Instead of having one image that is scaled up or down based on the viewport width, multiple images can be designed to more nicely fill the browser viewport. This element contains two tags: `<source>` and `<img>`
- The browser will look for the first `<source>` element where the media query matches the current viewport width, and then it will display the proper image (specified in the srcset attribute). The `<img>` element is required as the last child of the `<picture>` element, as a fallback option if none of the source tags matches.
- The `<picture>` element works "similar" to `<video>` and `<audio>`. You set up different sources, and the first source that fits the preferences is the one being used.

### CSS

- `scroll-behavior: smooth` - This property specifies whether to smoothly animate the scroll position, instead of a straight jump, when the user clicks on a link within a scrollable box.
- `position: fixed`
- `backdrop-filter: blur(5px)` - This property is used to apply a graphical effect to the area behind an element. To see the effect, the element or its background must be at least partially transparent.

## Authors

- [@bhoamikhona](https://github.com/bhoamikhona)
