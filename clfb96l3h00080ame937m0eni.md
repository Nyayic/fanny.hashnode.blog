---
title: "HTML Basics: Understanding HTML Tags"
seoTitle: "Understanding HTML Tags"
seoDescription: "HTML tags are used to structure and format content on a web page, and proper use of tags is important for creating well-structured and optimized webpages."
datePublished: Thu Mar 16 2023 15:15:32 GMT+0000 (Coordinated Universal Time)
cuid: clfb96l3h00080ame937m0eni
slug: html-basics-understanding-html-tags
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678978445469/5727e340-5ab1-4170-87cf-55902ec2a265.jpeg
tags: html, html5, 2articles1week, html-tags

---

HTML (HyperText Markup Language) is the foundation of every website on the internet. It is a markup language used to structure and display content on the web. Understanding HTML tags is essential for anyone looking to create or edit web content. In this article, we will discuss what HTML tags are, how they work, and provide examples of some of the most common HTML tags.

## What are HTML Tags?

HTML (Hypertext Markup Language) tags are elements used to structure and format content on a web page. HTML tags are enclosed in angle brackets and consist of a start tag, content, and an end tag.

The start tag indicates the beginning of the element, while the end tag indicates the end of the element. Some HTML tags are self-closing, meaning they do not require an end tag.

HTML tags are used to mark up the content of a web page so that web browsers can interpret and display it correctly.

HTML tags define different elements on a web page such as headings, paragraphs, images, links, and more. They are enclosed in angle brackets (&lt;&gt;) and can include attributes that provide additional information about the element.

## Common HTML tags and their uses

The &lt;html&gt; Tag

The `<html>` tag is one of the most fundamental tags in HTML, as it defines the beginning and end of an HTML document. This tag is required in every HTML document and it indicates to the browser that the following code is HTML markup.

All other tags in an HTML document must be placed inside the `<html>` tags. This is because the `<html>`tag acts as a container for all other HTML elements, such as the `<head>` and `<body>` tags.

The tag is used to contain information about the web page, such as the title, meta information, and links to other resources. The `<body>` tag contains the main content of the web page, including text, images, and other media.

By placing all other tags inside the `<html>` tags, you are creating a well-structured HTML document that is easy for browsers to read and display. It is important to follow this structure to ensure that your HTML document is properly formatted and that it is displayed correctly in web browsers.

### The &lt;head&gt; Tag

The `<head>` tag in HTML is used to contain information about the web page, such as the title, meta information, and links to other resources. This information is not displayed on the web page itself but is used by browsers to provide additional information about the page.

**Example:**

```xml
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
    <meta name="description" content="This is a description of my web page.">
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <h1>Welcome to My Web Page</h1>
    <p>This is some text on my web page.</p>
  </body>
</html>
```

In this example, the `<head>` tag contains three different types of information:

Title: The `<title>` tag sets the title of the web page, which is displayed in the browser's title bar and is used by search engines to index the page.

Meta information: The `<meta>` tag is used to provide additional information about the web page. In this example, the "description" meta tag provides a short description of the web page that can be used by search engines and other applications.

Links to other resources: The `<link>` tag is used to link to other resources, such as stylesheets, scripts, and icons. In this example, the `<link>` tag links to a stylesheet called `"styles.css"`.

By including this information in the `<head>` tag, you are providing important context and instructions for the web page. This helps search engines and other applications understand what the page is about and how it should be displayed.

### The &lt;title&gt;Tag

The `<title>` tag in HTML is used to specify the title of the web page. The text that is included between the `<title>` and `</title>` tags is displayed in the browser's title bar and are used by search engines to index the page.

**Example**:

```xml
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    <h1>Welcome to My Web Page</h1>
    <p>This is some text on my web page.</p>
  </body>
</html>
```

In this example, the `<title>` tag sets the title of the web page to "My Web Page". This text is displayed in the title bar of the browser and is used by search engines to index the page.

It is important to use descriptive and accurate titles for your web pages, as this can help users and search engines understand what the page is about.

For example, if you have a web page about gardening tips, you might use a title like "Gardening Tips for Beginners" or "10 Essential Gardening Tips for a Beautiful Garden". These titles give users an idea of what they can expect to find on the page and can help improve the page's search engine ranking.

In summary, the `<title>` tag is an important element of HTML that is used to specify the title of the web page. By using descriptive and accurate titles, you can help users and search engines understand what your web page is about and improve its visibility in search results.

### The &lt;body&gt; Tag

The `<body>` tag in HTML is used to contain the main content of the web page, including text, images, and other media. This is part of the HTML document that is displayed in the browser's window.

Here's an example of how the `<body>` tag might be used in an HTML document:

```xml
<!DOCTYPE html>
<html>
  <head>
    <title>My Web Page</title>
  </head>
  <body>
    <h1>Welcome to My Web Page</h1>
    <p>This is some text on my web page.</p>
    <img src="image.jpg" alt="An image on my web page">
  </body>
</html>
```

In this example, the `<body>` tag contains three different types of content:

**Text:** The `<h1>` and `<p>` tags are used to display text on the web page. The `<h1>` tag sets a heading for the page, while the `<p>` tag is used to display a paragraph of text.

**Images:** The `<img>` tag is used to display an image on the web page. In this example, the `<img>` tag links to an image called `"image.jpg"` and includes an `"alt"` attribute that provides a description of the image for users who cannot see it.

**Other media:** The `<body>` tag can also contain other types of media, such as audio or video files, or embedded content from other websites.

By including all of the main content of your web page in the `<body>` tag, you are creating a well-structured HTML document that is easy for browsers to read and display.

It is important to use appropriate HTML tags to structure your content and to provide descriptive attributes for images and other media to ensure that your web page is accessible and understandable for all users.

### The &lt;h1&gt; to &lt;h6&gt; Tags

In HTML, the h1 to h6 tags are used to define headings on a web page, with h1 being the largest and h6 being the smallest. These headings are important for structuring content and helping readers navigate the page.

Here are the different heading tags and their usage with examples:

h1 tag - This tag represents the most important heading on a page and should only be used once per page.

**Example:**

```xml
<!DOCTYPE html>
<html>
<head>
  <title>Example Page</title>
</head>
<body>
  <h1>Welcome to Example Page</h1>
  <p>This is a paragraph of text.</p>
</body>
</html>
```

h2 tag - This tag represents a heading of lesser importance than h1 and can be used multiple times on a page.

```xml
<!DOCTYPE html>
<html>
<head>
  <title>Example Page</title>
</head>
<body>
  <h1>Welcome to Example Page</h1>
  <h2>Section 1</h2>
  <p>This is a paragraph of text in section 1.</p>
  <h2>Section 2</h2>
  <p>This is a paragraph of text in section 2.</p>
</body>
</html>
```

h3 to h6 tags - These tags represent headings of even lesser importance than h2 and can also be used multiple times on a page.

```xml
<!DOCTYPE html>
<html>
<head>
  <title>Example Page</title>
</head>
<body>
  <h1>Welcome to Example Page</h1>
  <h2>Section 1</h2>
  <h3>Subsection 1.1</h3>
  <p>This is a paragraph of text in subsection 1.1.</p>
  <h3>Subsection 1.2</h3>
  <p>This is a paragraph of text in subsection 1.2.</p>
  <h2>Section 2</h2>
  <h3>Subsection 2.1</h3>
  <p>This is a paragraph of text in subsection 2.1.</p>
  <h4>Subsubsection 2.1.1</h4>
  <p>This is a paragraph of text in subsubsection 2.1.1.</p>
  <h5>Subsubsection h5</h5>
  <p>This is a paragraph of text in subsubsection 2.1.1.</p>
  <h6>Subsubsection h6</h6>
  <p>This is a paragraph of text in subsubsection 2.1.1.</p>
</body>
</html>
```

Note that using appropriate heading tags and structuring content with hierarchy can help improve the accessibility and readability of a web page.

### The &lt;p&gt; Tag

The "p" tag is a fundamental HTML element used to define paragraphs or blocks of text on a web page. Its purpose is to separate content into distinct sections, making it more readable and easier to understand for website visitors.

For example, if you have a webpage about the benefits of exercise, you may want to separate your content into distinct paragraphs. You could use the "p" tag to define each paragraph:

```xml
<p>Regular exercise has many benefits for your physical and mental health.</p>

<p>Exercise can help to reduce the risk of chronic diseases, such as heart disease and diabetes.</p>

<p>It can also improve your mood, boost your energy levels, and promote better sleep.</p>
```

When the browser renders the HTML document, each of these "p" tags creates a separate block of text with a line break above and below the paragraph. This makes it easier for visitors to read and understand the content on your page.

The "p" tag can also be used in conjunction with other HTML tags to create more complex layouts and structures on a web page. For example, you can use it within a "div" tag to create a block of text with a border:

```xml
<div class="textbox">
  <p>Exercise is essential for good health!</p>
</div>
```

In this example, the "div" tag creates a container element with a class of "textbox." The "p" tag is nested inside the "div" tag, defining the content within the container. This creates a visually distinct block of text with a border around it.

Overall, the "p" tag is a crucial tool for web developers who want to create well-organized and readable content on their websites. By using it effectively, you can make your content more accessible and engaging for your visitors.

### The &lt;a&gt; Tag

The "a" tag is an HTML element used to create hyperlinks on a web page. Hyperlinks are clickable links that allow users to navigate to other pages, files, or websites. The "a" tag is a crucial tool for creating a navigable and interconnected web.

To create a hyperlink using the "a" tag, you need to specify two attributes: "href" and "text." The "href" attribute defines the URL (Uniform Resource Locator) of the destination that the link should point to. The "text" attribute defines the text that should be displayed as a clickable link.

Here's an example of how to create a basic hyperlink using the "a" tag:

```xml
<a href="https://example.com">Click here to visit Example.com</a>
```

In this example, the "a" tag contains an "href" attribute with the URL of the website you want to link to. The text between the opening and closing "a" tags is the text that will be displayed as the clickable link.

You can also use relative URLs with the "a" tag to link to other pages or files on your own website. For example:

```xml
<a href="/about">About Us</a>
```

In this example, the "href" attribute contains a relative URL that links to a page on the same website with a path of "/about". When a user clicks on this link, they will be taken to the "About Us" page.

You can also use the "a" tag to create links to specific sections of a page using anchor tags. For example:

```xml
<a href="#section-1">Jump to Section 1</a>
```

In this example, the "href" attribute contains an anchor tag with the ID of a specific section of the page. When a user clicks on this link, they will be taken to that section of the page.

Overall, the "a" tag is an essential tool for web developers who want to create a navigable and interconnected web. By using it effectively, you can create meaningful links that allow users to explore and engage with your website.

### The&lt;img&gt;Tag

The `"img"` tag is an HTML element used to display images on a web page. It is a self-closing tag and does not require a closing tag. The "img" tag requires a "src" (source) attribute that specifies the location of the image file to be displayed.

Here is an example of how to use the "img" tag to display an image on a web page:

```xml
<img src="example.jpg" alt="Example Image">
```

In this example, the "src" attribute specifies the location of the image file `"example.jpg."` The "alt" attribute provides alternative text that is displayed if the image cannot be loaded or if the user is using a screen reader.

You can also include additional attributes with the "img" tag to specify the width and height of the image, as well as to add a border, change the alignment, and more.

```xml
<img src="example.jpg" alt="Example Image" width="500" height="300" border="1" align="center">
```

In this example, the "width" and "height" attributes specify the dimensions of the image in pixels. The "border" attribute adds a border around the image, and the "align" attribute centers the image horizontally on the page.

It is essential to optimize the size and format of images used on a web page to ensure fast loading times and minimize the impact on web page performance. You can use image optimization tools to compress and reduce the size of image files without compromising image quality.

Overall, the "img" tag is an essential tool for web developers who want to add visual elements to their web pages. By using it effectively, you can enhance the user experience and make your web pages more engaging and visually appealing.

### The &lt;ul&gt; and &lt;li&gt; Tags

The "ul" and "li" tags are HTML elements used to create unordered lists on a web page. Unordered lists are used to present a collection of items in no particular order.

Here is an example of how to use the "ul" and "li" tags to create a simple unordered list:

```xml
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

In this example, the `"ul"` tag defines the beginning and end of the unordered list, while the "li" tags define each item in the list. The numbers or bullet points are automatically added by the browser.

You can also use CSS (Cascading Style Sheets) to style the unordered list, such as changing the color or style of the bullet points or removing them altogether.

```xml
<ul style="list-style-type: square;">
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

In this example, The `"list-style-type"` property is set to `"square"` to change the style of the bullet points to squares.

You can also nest unordered lists within one another to create sub-lists.

```xml
<ul>
  <li>Item 1</li>
  <li>Item 2
    <ul>
      <li>Sub-item 1</li>
      <li>Sub-item 2</li>
    </ul>
  </li>
  <li>Item 3</li>
</ul>
```

In this example, a sub-list is created within "Item 2" by nesting a second "ul" and "li" tags.

Overall, the "ul" and "li" tags are essential tools for web developers who want to create structured and organized content on their web pages. By using them effectively, you can present information in a clear and easy-to-understand format for your users.

### The &lt;ol&gt; and &lt;li&gt; Tags

The `"ol"` and `"li"` tags are HTML elements used to create ordered lists on a web page. Ordered lists are used to present a collection of items in a specific order, such as in numerical or alphabetical order.

Here is an example of how to use the "ol" and "li" tags to create a simple ordered list:

```xml
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>
```

In this example, the "ol" tag defines the beginning and end of the ordered list, while the "li" tags define each item in the list. The numbers or alphabetical characters are automatically added by the browser.

You can also use CSS (Cascading Style Sheets) to style the ordered list, such as changing the color or style of the numbering or removing it altogether.

```xml
<ol style="list-style-type: lower-roman;">
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>
```

In this example, the `"list-style-type"` property is set to `"lower-roman"` to change the style of the numbering to lowercase Roman numerals.

You can also nest ordered lists within one another to create sub-lists.

```xml
<ol>
  <li>First item</li>
  <li>Second item
    <ol>
      <li>Sub-item 1</li>
      <li>Sub-item 2</li>
    </ol>
  </li>
  <li>Third item</li>
</ol>
```

In this example, a sub-list is created within the "Second item" by nesting a second "ol" and "li" tags.

Overall, the "ol" and "li" tags are essential tools for web developers who want to create structured and organized content on their web pages. By using them effectively, you can present information in a clear and easy-to-understand format for your users.

### The &lt;div&gt; Tag

The `"div"` tag is a fundamental HTML element used to create a container for other HTML elements. It is often used to group related content together and to apply styles or other attributes to the entire group of elements at once.

Here is an example of how to use the `"div"` tag to create a container for a group of HTML elements:

```xml
<div>
  <h2>Heading</h2>
  <p>This is a paragraph of text.</p>
  <ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
  </ul>
</div>
```

In this example, the "`div`" tag is used to group the heading, paragraph, and unordered list together. This allows you to apply styles or other attributes to the entire group of elements at once, such as setting the background color or adding a border.

You can also use multiple "`div`" tags to create more complex layouts on your web page.

```xml
<div class="container">
  <div class="row">
    <div class="col-md-6">
      <h2>Heading</h2>
      <p>This is a paragraph of text.</p>
    </div>
    <div class="col-md-6">
      <img src="image.jpg" alt="Image">
    </div>
  </div>
</div>
```

In this example, multiple `"div"` tags are used to create a container, row, and column layout for a heading, paragraph, and image. The classes `"container"`, "row", and `"col-md-6`" are from a popular CSS framework called Bootstrap, which helps to create responsive and flexible layouts for web pages.

Overall, the `"div"` tag is a versatile HTML element that allows web developers to create containers for groups of HTML elements, and to apply styles or other attributes to the entire group of elements at once.

## Summary

| Tag | Description |
| --- | --- |
| *&lt;html&gt;* | *Defines the root element of an HTML document* |
| *&lt;head&gt;* | *Contains meta-information about the HTML document, such as the title and links to stylesheets and scripts* |
| *&lt;title&gt;* | *Defines the title of the document, which appears in the browser's title bar* |
| *&lt;body&gt;* | *Contains the main content of the web page* |
| *&lt;h1&gt; to &lt;h6&gt;* | *Defines headings of different levels of importance* |
| *&lt;p&gt;* | *Defines a paragraph of text* |
| *&lt;a&gt;* | *Creates hyperlinks to other pages or resources* |
| *&lt;img&gt;* | *Inserts an image into the web page* |
| *&lt;ul&gt;* | *Defines an unordered list* |
| *&lt;ol&gt;* | *Defines an ordered list* |
| *&lt;li&gt;* | *Defines a list item* |
| *&lt;div&gt;* | *Defines a division or section of the web page* |
| *&lt;span&gt;* | *Defines a small inline section of the web page* |
| *&lt;table&gt;* | *Defines a table on the web page* |
| *&lt;tr&gt;* | *Defines a table row* |
| *&lt;th&gt;* | *Defines a table header cell* |
| *&lt;td&gt;* | *Defines a table data cell* |
| *&lt;form&gt;* | *Defines a form for user input* |
| *&lt;input&gt;* | *Creates an input field where users can enter data* |
| *&lt;select&gt;* | *Creates a dropdown list for user selection* |
| *&lt;option&gt;* | *Defines an option in a dropdown list* |
| *&lt;button&gt;* | *Defines a clickable button on the web page* |
| *&lt;textarea&gt;* | *Creates a text area for users to enter large amounts of text* |

*These are just a few of the many HTML tags available. By understanding how these tags work, you can create web pages that are well-structured and easy to read.*

In conclusion, HTML (Hypertext Markup Language) is a fundamental building block of web development. HTML tags are used to structure and format content on a web page, and proper use of tags is important for creating well-structured, accessible, and search engine-optimized web pages.

Some commonly used HTML tags include &lt;html&gt;, &lt;head&gt;, &lt;body&gt;, &lt;h1&gt; to &lt;h6&gt;, &lt;p&gt;, &lt;a&gt;, &lt;img&gt;, &lt;ul&gt;, &lt;ol&gt;, &lt;li&gt;, &lt;div&gt;, &lt;span&gt;, &lt;table&gt;, &lt;tr&gt;, &lt;th&gt;, &lt;td&gt;, &lt;form&gt;, &lt;input&gt;, &lt;select&gt;, &lt;option&gt;, &lt;button&gt;, and &lt;textarea&gt;.

By understanding and utilizing these tags effectively, developers can create engaging and effective websites that meet the needs of users and businesses alike.

Whether you are just starting with web development or looking to improve your existing skills, a solid understanding of HTML is essential. With its flexibility and power, HTML is sure to remain a key tool for web developers for years to come.