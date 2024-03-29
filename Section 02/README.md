# Section 02: HTML Fundamentals

**About:** In this section, we will learn the fundamental language of web development, which is HTML. We're going to learn HTML by building a small example project where you will learn all about the most import HTML elements e.g. Headings, Paragraphs, Lists, Images, Links, and more.

[Visit Site](https://bhoamikhona.github.io/html-css-bootcamp/Section%2002/index.html)
[Visit Challenge](https://bhoamikhona.github.io/html-css-bootcamp/Section%2002/challenge.html)

## Lessons Learned

- What is HTML?
  - HTML stands for HyperText Markup Language.
  - HTML is one of the core web technologies along with CSS and Javascript.
  - HTML is a markup language that web developers use to structure and describe the content of a webpage.
  - NOTE: HTML is not a programming language.
  - HTML consists of elements that describe different types of content:
    - paragraphs, links, headings, images, videos, etc.
  - Web browsers, such as Google Chrome, essentially understand HTML code and can render it as a final website, website that we can see in the browser.
- Anatomy of an HTML Element:
  - `<p>HTML is a Markup Language</p>`
  - HTML element is usually made up of 3 parts:
    - Opening Tag:
      - Name of the element wrapped in < and >
    - Content:
      - Content of the element which could be text or another element (child element). Some elements have no content and no closing tags (e.g. `<img>`).
    - Closing Tag:
      - Same as opening tag but, with a "/".
- HTML Document Structure
  - `<!DOCTYPE html>`
    - This tells the browser that this document uses HTML.
  - `<html></html>`
    - Each and every HTML document always needs to start with the HTML element.
    - Inside of the HTML element, we need one head element and one body element.
  - `<head></head>`
    - The head element is for things that are not visible in the browser window.
    - Head contains things like page title, additional information about the page, link to CSS files or other things.
  - `<body></body>`
    - Body is for all the elements that will be visible on the page.
  - `<title></title>`
- Text Elements
  - Headings
    - There is a hierarchy of headings, and we have 6 of them to choose from.
    - `<h1>Heading 1</h1>`
    - `<h2>Heading 2</h2>`
    - `<h3>Heading 3</h3>`
    - `<h4>Heading 4</h4>`
    - `<h5>Heading 5</h5>`
    - `<h6>Heading 6</h6>`
  - Paragraphs
    - `<p>This is a paragraph.</p>`
  - Bold
    - `<b>This is a bold text.</b>`
    - `<strong>This is a strong text.</strong>`
    - `<b>` vs `<strong>`
    - Use of `<b>` is not a good practice. It is an older HTML element and, starting in HTML 5, we should always use the `<strong>` element instead of `<b>`. The reason for that is that `<b>` doesn't have any so-called semantic meaning i.e. `<b>` is simply an element without a specific meaning. While on the other hand, the `<strong>` element means that this is really an important element that we want to stand out from the page.
  - Italic
    - `<i>This is italic text.</i>`
    - `<em>This is emphasis text.</em>`
    - `<i> vs <em>`
    - Similar to bold elements, `<i>` is simply a HTML element whereas `<em>` is a HTML element with semantic meaning therefore it is a good practice to use `<em>` instead of `<i>`.
  - Lists
    - Ordered List
      - `<ol><li>Item 1</li><li>Item 2</li><li>Item 3</li></ol>`
    - Unordered List
      - `<ul><li>Item 1</li><li>Item 2</li><li>Item 3</li></ul>`
- Comments
  - `<!-- This is a comment in HTML -->`
- Images and Attributes
  - `<img src="#" alt="alternative-text">`
  - Image element does not have any content which is why it does not have a closing tag.
  - Attributes are pieces of data which we can use to describe elements. There are lots of different attributes in HTML and one of them is `src` attribute.
  - The `src` attribute allows us to specify which image do we want the `<img>` tag to render.
  - Another attribute that we should never skip is the `alt` attribute, and `alt` stands for alternative-text. This text should describe what the image is about. This is very important for various reasons and one of them is that it will allow search engines such as Google Chrome to know what the image is about. Another important reason is that by specifying the description of the image, we can also allow blind people to use a website. So, users who use a screen reader will not see the image but, instead they will have the screen reader read the alternative text i.e. the image description to them. Another use case of alt-text is that if for some reason (e.g. src is wrong) the browser cannot find the image, it will render the alt-text instead of image. Never skip this attribute, it is alway good to write a good description.
  - `width` and `height` image attributes.
  - Attributes Learned:
    - `src`
    - `alt`
    - `height`
    - `width`
    - `lang` - This attribute specifies the language of the element's content.
    - `charset` - Specifies the character encoding for the HTML document.
    - `href`
    - `target="_blank"` - This attribute and value allows us to open the link in a new tab.
- `<meta>`
  - The meta tag defines metadata about an HTML document. Metadata is data (information) about data.
- Hyperlinks
  - `<a href="#">Link</a>`
  - One of the fundamental building blocks of the internet are "hyperlinks", or for short "links". Links are what actually enables the internet to be a world wide web. Without links between pages, there would be no web.
  - Links can be placed into two big categories:
    - Internal Links i.e. links pointing to other pages in our own website.
    - External Links i.e. links point to other websites.
- Structuring Our Page
  - `<nav></nav>`
  - `<header></header>`
  - `<article></article>`
  - `<footer></footer>`
  - `<div></div>`
  - `<aside></aside>`
    - `<aside>` element is usually used for some secondary information that complements the information in the main part of the page. A lot of times, `<aside>` element is used as sidebar but, it doesn't necessarily have to be that way.
- HTML entity
  - `&copy;` - copyright symbol
  - `&rarr;` - right arrow symbol
- Semantic HTML
  - In HTML, when we talk about semantics, what we mean is that certain elements have actually a meaning or a purpose attached to them.
  - When we think about a certain HTML element, we should not think about what the element looks like as it's rendered on the page but instead, we should think about what that element actually means and what it stands for. That is basically the definition of semantic HTML.
  - Not all elements in HTML are semantic.
  - Semantic HTML is used for Search Engine Optimization i.e. Google or any other search engine will be able to better understand the content on your webpage using Semantic HTMl and also, it used for Accessibility purposes.
- `<button>Click Me</button>`

## Screenshots

![1](https://user-images.githubusercontent.com/50435319/225617905-a99c1710-78c3-4225-9df0-47f5e8889d7a.PNG)
![2](https://user-images.githubusercontent.com/50435319/225617908-ebaab405-7162-463c-9528-fd74f6bf6df7.PNG)

## Authors

- [@bhoamikhona](https://github.com/bhoamikhona)
