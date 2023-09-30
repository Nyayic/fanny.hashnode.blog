---
title: "How to use CSS media queries to Create a Responsive Website"
datePublished: Sat Sep 30 2023 05:00:09 GMT+0000 (Coordinated Universal Time)
cuid: cln5kdunt000109jrapvc3g7x
slug: how-to-use-css-media-queries-to-create-a-responsive-website
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695910445490/8319353a-3499-40d5-b720-6adf6d820db4.jpeg
tags: media-queries, css-frameworks, css, 2articles1week

---

Responsive web design (RWD) is a web design approach that ensures that a website looks good and functions well on all devices, from desktop computers to smartphones.

CSS media queries are a key component of RWD, as they allow you to apply different CSS styles to your website based on the characteristics of the device or browser that is being used to view it.

### **What is a media query?**

A media query is a CSS rule that allows you to apply different CSS styles to your website based on the characteristics of the device or browser that is being used to view it.

Media queries can be used to target a wide range of device and browser features, including screen size, orientation, resolution, and color depth.

### **How to use media queries**

To use a media query, you start by using the `@media` rule. This rule is followed by a media feature and a value.

For example, the following media query will apply the CSS styles that follow it to all devices with a screen width of 600 pixels or less:

```css
@media (max-width: 600px) {
  /* CSS styles for small screens */
}
```

You can also use multiple media features in a single media query. For example, the following media query will apply the CSS styles that follow it to all devices with a screen width of 600 pixels or less and a screen height of 400 pixels or less:

```css
@media (max-width: 600px) and (max-height: 400px) {
  /* CSS styles for small screens and small heights */
}
```

### **Media query features**

There is a wide range of media query features that you can use to target different devices and browser features. Some of the most common media query features include:

* `width`: Specifies the width of the viewport.
    
* `height`: Specifies the height of the viewport.
    
* `orientation`: Specifies the orientation of the device, either `portrait` or `landscape`.
    
* `resolution`: Specifies the resolution of the device's display.
    
* `color-index`: Specifies the number of colors that the device's display can display.
    
* `aspect-ratio`: Specifies the aspect ratio of the device's display.
    
* `device-pixel-ratio`: Specifies the pixel density of the device's display.
    
* `pointer-events`: Specifies whether the device has a pointer device, such as a mouse or touchscreen.
    
* `hover`: Specifies whether the device has a hover capability, such as a mouse.
    
* `touch`: Specifies whether the device has a touchscreen.
    

### **Examples of CSS media queries**

Here are some examples of how to use CSS media queries to create a responsive website:

**Change the font size for small screens:**

```css
@media (max-width: 600px) {
  body {
    font-size: 16px;
  }
}
```

**Hide a navigation bar for small screens:**

```css
@media (max-width: 600px) {
  #navigation {
    display: none;
  }
}
```

**Change the layout of a page for small screens:**

```css
@media (max-width: 600px) {
  .main-content {
    width: 100%;
  }
  .sidebar {
    display: none;
  }
}
```

**Use different images for different screen sizes:**

```css
@media (max-width: 600px) {
  .my-image {
    background-image: url('my-image-small.jpg');
  }
}

@media (min-width: 601px) {
  .my-image {
    background-image: url('my-image-large.jpg');
  }
}
```

**Use media queries to target specific devices and features:**

```css
@media (max-width: 600px) and (device-pixel-ratio: 2) {
  /* CSS styles for high-resolution smartphones */
}

@media (min-width: 768px) and (max-width: 1024px) and (orientation: landscape) {
  /* CSS styles for landscape tablets */
}
```

### **Best practices for using CSS media queries**

Here are some best practices for using CSS media queries:

* **Use a mobile-first approach.** This means designing your website for mobile devices first and then adding additional styles for larger screens. This approach helps to ensure that your website is always accessible and usable, even on small devices.
    
* **Use relative units for your layout.** This will help your website to scale gracefully to different screen sizes. For example, instead of using a fixed width of 960 pixels for your main content area, use a relative unit such as 90%. This will ensure that your main content area is always 90% of the available width, regardless of the screen size.
    
* **Use media queries to target specific devices and features.** Don't just use media queries to target screen size. You can also use them to target specific devices, such as tablets or smartphones. You can also use media queries to target specific features, such as high-resolution displays or touchscreens.
    
* **Test your website on different devices and screen sizes.** Once you have implemented media queries, it is important to test your website on a variety of devices and screen sizes to ensure that it looks good and works properly on all of them.
    

### **Advanced media queries**

In addition to the basic media queries that we have discussed so far, there are also several more advanced media queries that you can use. These advanced media queries can be used to target more specific devices and features and to create more complex responsive designs.

Some examples of advanced media queries include:

* **Media queries that target specific devices:**
    

```css
@media (device-aspect-ratio: 16/9) {
  /* CSS styles for 16:9 devices */
}

@media (device-name: "iPhone") {
  /* CSS styles for iPhones */
}
```

* **Media queries that target specific features:**
    

```css
@media (max-device-width: 414px) and (max-device-height: 896px) and (orientation: portrait) {
  /* CSS styles for iPhone 6 and 7 in portrait orientation */
}

@media (min-device-width: 1024px) and (max-device-width: 1366px) and (orientation: landscape) {
  /* CSS styles for 1366x768 displays in landscape orientation */
}
```

* **Media queries that use multiple features:**
    

```css
@media (min-device-width: 768px) and (max-device-width: 1024px) and (orientation: landscape) and (-webkit-min-device-pixel-ratio: 2) {
  /* CSS styles for landscape tablets with high-resolution displays */
}
```

CSS media queries are a powerful tool for creating responsive websites. By using media queries, you can ensure that your website looks good and works well on all devices and screen sizes.

Here are some additional tips for using CSS media queries effectively:

* **Use a media query library.** There are several media query libraries available that can help you to write and maintain your media queries.
    
    These libraries can provide you with a set of pre-defined media queries, as well as tools for generating your custom media queries.
    
* **Use progressive enhancement.** Progressive enhancement is a web design approach that involves building a basic website that works on all devices and then adding additional features and functionality for devices that support them. This approach helps to ensure that your website is always accessible and usable, even on older devices and devices with limited capabilities.
    
* **Test your website thoroughly.** Once you have implemented media queries, it is important to test your website thoroughly on a variety of devices and screen sizes to ensure that it looks good and works properly on all of them. You should also test your website in different browsers and browser versions.
    

**Happy Coding!**