# Section 07: Omnifood Project - Setup and Desktop Version

**About:** In this section, I'm going to take all the HTML, CSS, and Design Skills that I've been learning and apply them in order to build a huge, real world project called Omnifood. Omnifood is a fictional startup that uses AI to create and deliver custome healthy meal plans. But, right now, before they can launch their product, they need a beautiful, modern, and clean website which will make them look like a professional and trustworthy company. That is where I come in, I am pretending that I am hired by Omnifood to design and build their marketing website using HTML and CSS and build this project. Omnifood provides all the content for the website and now I've just got to design and implement it.

## Lessons Learned

- The 7 Steps to a Great Website:
  - 01: Define
    - Define **who** the website is for?
    - Define **what** the website is for?
    - Define **target audience**. Be very specific if possible. (This could also come from your client)
  - 02: Plan
    - Plan and gather **website content**: text, images, videos, etc. (This will usually come from your client)
    - For bigger sites, plan out the **sitemap and content hierarchy**.
    - Based on content, plan **sections** on each web-page.
    - Define **Website Personality**.
  - 03: Sketch
    - Think about what **components** are needed and how you can use them in **layout patterns**.
    - **Sketch design ideas** using pen and paper or a design software like Balsamiq.
    - This is an **iterative process**, don't set anything in stone yet, just keep experimenting with different components and layouts until you reach at a first good solution.
    - You don't neet to make it perfect, this is supposed to be low fidelity, like a wireframe. At some point you will be ready to move to HTML and CSS.
  - 04: Design and Build
    - Use decisions, content, and sketches from steps 1, 2, and 3 to design and build the website with HTML and CSS.
    - You should have the layout and components from step 3, in this step, you just need to implement those layouts and components using HTML and CSS.
    - Create the design based on selected website personality, the design guidelines from section 04, and by taking inspirations from other web designers.
    - Use the client's branding (if it already exists) for design decisions whenever possible: colors, typography, icons, etc.
  - 05: Test and Optimize
    - Make sure website works well in **all major browsers** (Chrome, Firefox, Safari, Edge)
      - Hopefully, not in the (old school) Internet Explorer because then most of the things won't work on there.
    - Test the website on **actual mobile devices**, not just in DevTools
    - **Optimize** all **images**, in terms of dimensions and file size.
    - Fix simple **accessibility** problems (e.g. color contrast)
    - Run the **Lighthouse performance test** in Chrome DevTools and try to fix reported issues.
    - Think about **Search Engine Optimization (SEO)**
  - 06: Launch
    - Once all work is done, everything is perfect, and you got approval, it's time to launch the website i.e. host your website on a hosting platform.
    - Choose and buy a great domain name, one that represents the brand well, is memorable, and easy to write.
  - 07: Maintain and Update
    - Launching is not the end.
    - Keep the website content updated over time. If you're working with a client, you can create a monthly maintenance contract.
    - Install **analytics software** (e.g. Google Analytics or Fathom) to get statistics about website users. This may **inform future changes** in the site structure and content.
    - A **blog** that is updated regularly is a good way to keep users coming back, and is also good for SEO.
- Responsive Web Design Principles
  - Responsive web design is a technique to make a web-page adjust its layout and visual style to any possible size (window or viewport size).
  - In practice, this means that responsive design makes websites usable on all devices, such as desktop computers, tablets, and mobile phones.
  - It's a set of practices, not a separate technology. It is all just CSS.
  - There are essentially 4 big ingredients to responsive designs v.i.z. 1. Fluid Layouts 2. Responsive Units 3. Flexible Images and 4. Media Queries
    - Fluid Layouts:
      - This allows webpage to adapt to the current viewport width (or height)
      - Use % (or vh / vw) unit instead of px for elements that should adapt to viewport (usually layout)
      - Use `max-width` instead of width
    - Responsive Units:
      - Use rem unit instead of px for most lengths
      - To make it easy to scale the entire layout down (or up) automatically
      - **Helpful Trick:** Set 1rem to 10px for easy calculations.
    - Flexible Images:
      - By default, images don't scale automatically as we change the viewport so, we need to fix that.
      - Always use % for image dimensions, together with the max-width property.
    - Media Queries:
      - Bring responsive sites to life.
      - To change CSS styles onc ertain viewport widths (called breakpoints).
  - NOTE: Media Queries alone are useless, we need to create fluid layouts from the very beginning, and same is true to responsive units and flexible images. In fact, we only write media queries only at the end of building a certain page or a certain component.
- Desktop-First vs. Mobile-First Development Approach
- How rem and max-width work

  - `max-width` - If the container's width is larger than the specified max-width, then the width of the element is equal to the value that was specified for max-width. However, if the container's width is less than the specified max-width, then the width of the element will be 100% of the container element width.
  - `rem` unit - rem stands for 'root element font size'. The root of the document is HTML element i.e. the parent element of all the other elements. If we don't decide any font size on the HTML element, then 1 rem = 16 px and 16 px is the default browser font-size.
  - To reset from 1 rem = 16 px to 1 rem = 10 px, simply set `font-size = 10px` in the html tag.
  - NOTE: This is not perfect because we will not respect the user's browser's font size. Let's say that user changes the default from 16px to 20px, then of course they would expect that the font-size on our page would increase but, with the set up mentioned above, that won't happen. So, no matter what the user would set the font-size to now, we would always have our root font-size at 10px. This will create huge usability problems who have to increase or decrease the font size of their browsers. In order to address that issue, use percentage of the default font-size of browser. 10 px divided by 16 px = 62.5% i.e. 10 px = 62.5% so, in order to set font-size as 10 px in percentage, set it equal to 62.5% and it should adapt to the user's browser should they decide to increase or decrease the font-size on their browser.

- Creating and using general reusable CSS classes

### HTML

- A link is used for going somewhere on the page or goint to other pages while a button element should only be used for actions i.e. if something happens that is not related to navigation.
- `<figure></figure>` - The figure tag specifies self-contained content like illustrations, diagrams, photos, code listings, etc. While the content of the figure element is related to the main flow, its position is independent of the main flow, and if removed, it should not affect the flow of the document.
- `<figcaption></figcaption>` - The figcaption tag defines a caption for a `<figure>` element. It can be placed as the first or last child of the `<figure>` element.
- `role` attribute
- `aria-label`
- forms:
  - `<input>`
    - input type text
    - input type email
    - input attributes:
      - id, type, placeholder, required
  - `<label>`
    - label attributes:
      - for
  - `<select>`
    - select attributes:
      - id
      - required
    - `<option>`
      - option attributes:
        - value
- `tel:` and `mailto:` when using anchor tags
- `<br>` - Line break

### CSS

- `transition: all 3s` - CSS transition property allows you to change property values smoothly, over a given duration.
  - To create a transition effect, you must specify 2 things: 1. the CSS property you want to add an effect to and 2. the duration of the effect.
  - NOTE: If the duration is not specified, the transition will have no effect because, the default value is 0.
- `filter: grayscale(100%)` - The filter property defines visual effects (like blur and saturation) to an element (often image)
  - filter property values:
    - `none` - Default, no effects.
    - `blur(px)` - Applies a blur effect to the image. A larger value will create more blur. If no value is specified, 0 is used.
    - `brightness(%)` - Adjusts the brightness of the image. 0 will make is completely black and 100% is default and represents the original image. Values over 100% will provide brighter results.
    - `contrast(%)` - Adjusts the contrast of the image. 0 will make the image completely black. 100% is default, and represents the original image. Values over 100% will provide results with more contrast.
    - `drop-shadow(8px 8px 10px red)` - Applies a drop shadow effect to the image. This filter is similar to the box-shadow property.
    - `grayscale(%)` - Converts the image to grayscale. 0 is default and represents the original image. 100% will make the image completely gray (used for black and white images). Negative values are not allowed.
    - `hue-rotate(deg)` - Applies a hue rotation on the image. The value defines the number of degrees around the color circle the image samples will be adjusted. 0deg is default and represents the original image. Maximum value is 360deg
    - `invert(%)` - Inverts the samples in the image. 0 is default and represents the original image. 100% will make the image completely inverted. Negative values are not allowed.
    - `opacity(%)` - Sets the opacity level for the image. The opacity-level describes the transparency-level, where 0 is completely transparent and 100% is default and represents the original image. Negative values are not allowed.
    - `saturate(%)` - Saturates the image. 0 will make the image completely unsaturated. 100% is default and represents the original image. Values over 100% provides super-saturated results. Negative values are not allowed.
    - `sepia(%)` - Converts the image to sepia. 0 is default and represents the ogriginal image. 100% will make the image completely sepia. Negative values are not allowed.
    - `url()` - The url() function takes the location of an xml file that specifies an SVG filter, and may include an anchor to a specific filter element.
    - `initial` - Sets the property to its default value.
    - `inherit` - Inherits this property from its parent element.
- `opacity: 0.5` - The opacity propert specifies the opacity/transparency of an element. The value can go from 0.0 to 1.0. The lower the value, the more transparent.

- `currentColor` keyword - The currentColor keyword refers to the value of the color property of an element.

- `transparent` keyword - The transparent keyword is used to make a color transparent. This is often used to a make transparent background color for an element. The keyword is equal to rgba(0,0,0,0)

- `:not()` - The `:not()` CSS pseudo class represents elements that do not match a list of selectors. Since it prevents specific items from being selected, it is known as the negation pseudo-class.

- `inherit` keyword - The inherit keyword specifies that a property should inherit its value from its parent element. It can be used for any CSS property, and on any HTML element.

- `:focus` - The focus selector is used to select the element that has focus. It is allowed on elements that accept keyboard event or other user inputs.

- `outline: 1px solid black` - The outline property draws an outline around elements, outside the borders, to make the element "stand out". It is a shorthand for `outline-width`, `outline-style`, and `outline-color`. If outline-color is omitted, the color applied will be the color of the text.
  - NOTE: Outline is not a part of the box model.

## Secreenshots

### Navigation Bar & Hero Section

![navigation bar and hero section](https://user-images.githubusercontent.com/50435319/226882014-41f29d8c-824c-451a-8d82-d947cea42f3c.PNG)

### Featured In Section

![featured in](https://user-images.githubusercontent.com/50435319/226882039-cb4e40b1-1913-4ddc-a430-d0d48873a8bf.PNG)

### How It Works Section

![how it works](https://user-images.githubusercontent.com/50435319/226882052-cb09c936-f0a6-4dc5-bcbf-12d0f6c7ca6a.PNG)
![how it works 2](https://user-images.githubusercontent.com/50435319/226882048-a4f5c62b-da7b-43e1-bfd9-d3985698163a.PNG)

### Meals Section

![meals](https://user-images.githubusercontent.com/50435319/226882053-5400db91-2bd0-415c-a972-d30a94044d1b.PNG)

### Pricing Section

![pricing](https://user-images.githubusercontent.com/50435319/226882024-78616898-c7be-421c-942b-ce421cccd774.PNG)

### Features

![features](https://user-images.githubusercontent.com/50435319/226882041-571ceda0-e1b5-49ba-b14f-fe86df4e862d.PNG)

### Call To Action (CTA) Section

![cta](https://user-images.githubusercontent.com/50435319/226882029-b6ef73df-31dc-4733-b8a2-2ce4004e9ae3.PNG)

### Footer

![footer](https://user-images.githubusercontent.com/50435319/226884745-ad998327-663f-45ae-a0d8-38f8291687a2.PNG)

## Authors

- [@bhoamikhona](https://github.com/bhoamikhona)
