# A-Frame HTML Shader

A shader to render 2D HTML and CSS to a texture for [A-Frame](https://aframe.io). This is an update using html2canvas v1.0rc which will render svg.
Important note:
- svg must have size (in css)
- must add data-html2canvas-ignore="true" into <a-scence> (look at example below)
  
![ScreenShot](https://github.com/Zipexpo/aframe-html-shader/blob/master/examples/demo.PNG)

All information go to [mayognaise github](https://github.com/mayognaise/aframe-html-shader)

### Browser Installation

Install and use by directly including the [browser files](dist):

```html
<head>
  <title>My A-Frame Scene</title>
  <script src="https://aframe.io/releases/0.8.2/aframe.min.js"></script>
  <script src="yourlibpath/aframe-html-shader.min.js"></script>
</head>

<body>
  <a-scene data-html2canvas-ignore="true">
    <a-entity geometry="primitive: box" material="shader: html; target: #htmlElement"></a-entity>
  </a-scene>

  <div style="width: 100%; height: 100%; position: fixed; left: 0; top: 0; z-index: -1; overflow: hidden">
    <div id="htmlElement" style="background: #F8F8F8; color: #333; font-size: 48px">Hello, HTML!</div>
  </div>
</body>
```
