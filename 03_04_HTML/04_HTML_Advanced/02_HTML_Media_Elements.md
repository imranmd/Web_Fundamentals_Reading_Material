**HTML Audio, Video, Canvas, SVG**

**Introduction:**

HTML provides powerful elements to incorporate multimedia and graphics into webpages. In this tutorial documentation, we will learn about HTML audio, video, canvas, and SVG elements. These elements allow you to add audio and video content, draw graphics, and display scalable vector graphics on your webpages.

**HTML Audio Element:**

The `<audio>` element is used to embed audio content in a webpage. You can specify the audio source using the `src` attribute and provide fallback content between the opening and closing tags for browsers that do not support the audio element.

**Syntax for HTML Audio Element:**

```html
<audio src="audio.mp3" controls>
  Your browser does not support the audio element.
</audio>
```

**Working Example - HTML Audio Element:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Audio Example</title>
</head>
<body>
  <h1>Audio Example</h1>
  <audio src="sample.mp3" controls>
    Your browser does not support the audio element.
  </audio>
</body>
</html>
```

**HTML Video Element:**

The `<video>` element is used to embed video content in a webpage. Similar to the audio element, you can specify the video source using the `src` attribute and provide fallback content between the opening and closing tags for browsers that do not support the video element.

**Syntax for HTML Video Element:**

```html
<video src="video.mp4" controls>
  Your browser does not support the video element.
</video>
```

**Working Example - HTML Video Element:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Video Example</title>
</head>
<body>
  <h1>Video Example</h1>
  <video src="sample.mp4" controls>
    Your browser does not support the video element.
  </video>
</body>
</html>
```

**HTML Canvas Element:**

The `<canvas>` element is used to draw graphics and animations on a webpage using JavaScript. It provides a drawing context that allows you to create shapes, lines, colors, and perform various transformations.

**Syntax for HTML Canvas Element:**

```html
<canvas id="myCanvas" width="200" height="100">
  Your browser does not support the canvas element.
</canvas>
```

**Working Example - HTML Canvas Element:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML Canvas Example</title>
</head>
<body>
  <h1>Canvas Example</h1>
  <canvas id="myCanvas" width="200" height="100">
    Your browser does not support the canvas element.
  </canvas>

  <script>
    var canvas = document.getElementById("myCanvas");
    var ctx = canvas.getContext("2d");
    ctx.fillStyle = "blue";
    ctx.fillRect(10, 10, 150, 80);
  </script>
</body>
</html>
```

**HTML SVG Element:**

The `<svg>` element is used to display scalable vector graphics on a webpage. SVG graphics can be scaled without losing quality, making them ideal for various graphic elements.

**Syntax for HTML SVG Element:**

```html
<svg width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="red" />
</svg>
```

**Working Example - HTML SVG Element:**

```html
<!DOCTYPE html>
<html>
<head>
  <title>HTML SVG Example</title>
</head>
<body>
  <h1>SVG Example</h1>
  <svg width="100" height="100">
    <circle cx="50" cy="50" r="40" fill="red" />
  </svg>
</body>
</html>
```

**Additional Resources:**

1. MDN Web Docs - HTML Audio and Video: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio, https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video
2. MDN Web Docs - HTML Canvas and SVG: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas, https://developer.mozilla.org/en-US/docs/Web/SVG

**Summary:**

HTML provides elements like `<audio>`, `<video>`, `<canvas>`, and `<svg>` to enrich your webpages with multimedia content, graphics, and animations. By using these elements, you can create engaging and interactive web experiences for your users. Experiment with different media types, draw graphics, and display scalable vector graphics to enhance your web projects. Happy coding!