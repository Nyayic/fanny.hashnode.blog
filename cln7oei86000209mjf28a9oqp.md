---
title: "Advanced CSS Media Query Techniques"
datePublished: Sun Oct 01 2023 16:28:10 GMT+0000 (Coordinated Universal Time)
cuid: cln7oei86000209mjf28a9oqp
slug: advanced-css-media-query-techniques
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1706193382450/08b59971-9ab8-47e6-9489-c31466c0435f.png
tags: media-queries, css, 2articles1week

---

CSS media queries are a powerful tool for creating responsive web designs. They allow you to apply different styles to your website depending on the device or screen size that it is being viewed on.

This ensures that your website looks good and functions well on all devices, from smartphones to desktop computers.

## **Viewport Units**

Viewport units are a type of CSS unit that is relative to the size of the viewport. This means that they will scale up or down depending on the size of the device that the website is being viewed on.

There are three types of viewport units:

* `vw`: viewport width
    
* `vh`: viewport height
    
* `vmin`: the smaller of `vw` and `vh`
    
* `vmax`: the larger of `vw` and `vh`
    

Viewport units can be used in media queries to create responsive layouts that will adapt to any screen size. For example, the following media query will change the font size of the `h1` element to 2vw on devices with a viewport width of 600px or less:

```css
@media (max-width: 600px) {
  h1 {
    font-size: 2vw;
  }
}
```

## **The** `calc()` Function

The `calc()` function allows you to perform mathematical operations on CSS values. This can be useful for creating complex media queries that target specific device sizes or screen resolutions.

For example, the following media query will change the font size of the `h1` element to 20px on devices with a viewport width of 320px or less:

```css
@media (max-width: 320px) {
  h1 {
    font-size: calc(20px + 1vw);
  }
}
```

## **Orientation Media Queries**

Orientation media queries allow you to target specific device orientations, such as landscape or portrait mode. This can be useful for creating responsive layouts that look good on both phones and tablets.

For example, the following media query will change the width of the `main` element to 100% on devices in portrait mode:

```css
@media (orientation: portrait) {
  main {
    width: 100%;
  }
}
```

## **Multiple Media Queries**

You can combine multiple media queries into a single rule using the `and` and `or` operators. This allows you to create complex media queries that target specific devices or screen sizes.

For example, the following media query will change the font size of the `h1` element to 20px on devices with a viewport width of 320px or less and a device pixel ratio of 2 or more:

```css
@media (max-width: 320px) and (device-pixel-ratio: 2) {
  h1 {
    font-size: 20px;
  }
}
```

## **The** `not()` Operator

The `not()` operator allows you to create media queries that target devices that do not meet certain criteria. For example, the following media query will change the font size of the `h1` element to 20px on all devices except for devices with a viewport width of 320px or less:

```css
@media (not (max-width: 320px)) {
  h1 {
    font-size: 20px;
  }
}
```

## **The** `only` Operator

The `only` operator allows you to create media queries that target devices that meet only certain criteria. For example, the following media query will change the font size of the `h1` element to 20px on devices with a viewport width of 320px or less and no other media features:

```css
@media only (max-width: 320px) {
  h1 {
    font-size: 20px;
  }
}
```

## **Advanced Media Query Use Cases**

Here are a few examples of how to use advanced media queries to create more responsive and user-friendly web designs:

* **Use viewport units to create responsive layouts.** As mentioned above, viewport units are a type of CSS unit that is relative to the size of the viewport. This means that they will scale up or down depending on the size of the device.
    
* **Use the** `calc()` function to create complex media queries. The `calc()` function allows you to perform mathematical operations on CSS values. This can be useful for creating complex media queries that target specific device sizes or screen resolutions.
    
    For example, the following media query will change the font size of the `h1` element to 20px on devices with a viewport width of 320px or less, but only if the device pixel ratio is greater than or equal to 2:
    
* ```css
      @media (max-width: 320px) and (device-pixel-ratio: >= 2) {
        h1 {
          font-size: calc(20px + 1vw);
        }
      }
    ```
    
    **Use orientation media queries to create responsive layouts for different device orientations.**
    
    Orientation media queries allow you to target specific device orientations, such as landscape or portrait mode.
    
    This can be useful for creating responsive layouts that look good on both phones and tablets.
    
    For example, the following media query will change the width of the `main` element to 100% on devices in landscape mode:
    
* ```css
      @media (orientation: landscape) {
        main {
          width: 100%;
        }
      }
    ```
    
    **Use multiple media queries to create complex media queries that target specific devices or screen sizes.**
    
    You can combine multiple media queries into a single rule using the `and` and `or` operators. This allows you to create complex media queries that target specific devices or screen sizes.
    
    For example, the following media query will change the font size of the `h1` element to 20px on devices with a viewport width of 320px or less and a device pixel ratio of 2 or more, and only if the device is in portrait mode:
    
* ```css
      @media (orientation: portrait) and (max-width: 320px) and (device-pixel-ratio: >= 2) {
        h1 {
          font-size: 20px;
        }
      }
    ```
    
    **Use the** `not()` operator to create media queries that target devices that do not meet certain criteria. The `not()` operator allows you to create media queries that target devices that do not meet certain criteria.
    
    For example, the following media query will change the font size of the `h1` element to 20px on all devices except for devices with a viewport width of 320px or less and a device pixel ratio of 2 or more:
    
* ```css
      @media not (orientation: portrait) and (max-width: 320px) and (device-pixel-ratio: >= 2) {
        h1 {
          font-size: 20px;
        }
      }
    ```
    
    Use the only operator to create media queries that target devices that meet only certain criteria. The only operator allows you to create media queries that target devices that meet only certain criteria.
    
    For example, the following media query will change the font size of the h1 element to 20px on devices with a viewport width of 320px or less and no other media features:
    
* ```css
      @media only (max-width: 320px) {
        h1 {
          font-size: 20px;
        }
      }
    ```
    
    Here are a few additional tips for using advanced CSS media queries:
    
    * **Use a media query testing tool.** There are a number of media query testing tools available online that can help you test your media queries and make sure that they are working as expected.
        
    * **Use feature detection.** Feature detection is a technique for detecting the presence or absence of a specific feature on a device. This can be useful for creating media queries that target specific devices or browsers.
        
    * **Use progressive enhancement.** Progressive enhancement is a design philosophy that advocates building websites for the most basic browsers and then adding features and functionality for more advanced browsers. This approach can help you ensure that your website is accessible to all users, regardless of their device or browser.
        
    
    Happy Coding!