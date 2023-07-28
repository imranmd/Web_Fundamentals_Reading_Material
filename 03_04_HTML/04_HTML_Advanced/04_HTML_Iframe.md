**HTML Iframe**

**Introduction:**

An HTML iframe (inline frame) is used to embed another HTML document or webpage within the current document. It allows you to display content from another source, such as a video, map, or external website, directly on your webpage. Iframes are commonly used to integrate external content seamlessly into a webpage without affecting the layout and styling of the parent page.

**Why Use HTML Iframes:**

HTML iframes are useful in scenarios where you want to display external content while keeping it isolated from the parent page's layout and styles. They allow you to embed content from different sources, such as third-party widgets, maps, or videos, into your webpage.

**Syntax for HTML Iframe:**

```html
<iframe src="URL" width="width" height="height" title="description"></iframe>
```

**Attributes:**

- `src`: Specifies the URL of the content to be displayed in the iframe.
- `width`: Specifies the width of the iframe in pixels or as a percentage.
- `height`: Specifies the height of the iframe in pixels or as a percentage.
- `title`: Provides a description of the iframe for accessibility purposes.

**Working Example - HTML Iframe:**

Let's create a working example to demonstrate how to use an iframe to embed a YouTube video.

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Iframe Example</title>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <p>Check out this cool video:</p>
  <iframe
    width="560"
    height="315"
    src="https://www.youtube.com/embed/dQw4w9WgXcQ"
    title="YouTube video player"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
  ></iframe>
</body>
</html>
```

**Additional Resources:**

1. MDN Web Docs - HTML iframe Element: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe
2. W3Schools - HTML iframe Tag: https://www.w3schools.com/tags/tag_iframe.asp

**Summary:**

HTML iframes provide a convenient way to embed external content within a webpage, such as videos, maps, or third-party widgets. By using the `<iframe>` element and providing the appropriate URL, width, height, and title attributes, you can seamlessly integrate external content into your website. Be cautious when embedding external content, and ensure it is from trusted sources to maintain the security and integrity of your webpage. Happy iframe embedding!