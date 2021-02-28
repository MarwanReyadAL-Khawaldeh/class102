Chart.js, Canvas


**Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang them into use as a layout tool. They’re easier to look at and convey data quickly, but they’re not always easy to create.**


![chart](https://lh3.googleusercontent.com/proxy/0frFnEtaxxbFrWEKzD9AjfWsts3MvqSTHhHa2bMZSg3kEdC8t75prOUXjQ2dcr8wZ9LivdGMbSAilj603L30Wvj0dFTW9un6kENbwbGwSoald43LTbL-)


***Creating a Chart***

It's easy to get started with Chart.js. All that's required is the script included in your page along with a single <canvas> node to render the chart.

**Contributing**
Before submitting an issue or a pull request to the project, please take a moment to look over the contributing guidelines first.

**License**
![styling](https://i.ytimg.com/vi/EyZhXxoZqto/maxresdefault.jpg)

Chart.js is available under the MIT license.

> `The <canvas> element`

`At first sight a <canvas> looks like the <img> element, with the only clear difference being that it doesn't have the src and alt attributes. Indeed, the <canvas> element has only two attributes, width and height. These are both optional and can also be set using DOM properties. When no width and height attributes are specified, the canvas will initially be 300 pixels wide and 150 pixels high. The element can be sized arbitrarily by CSS, but during rendering the image is scaled to fit its layout size: if the CSS sizing doesn't respect the ratio of the initial canvas, it will appear distorted.`



> Fallback content
`Providing fallback content is very straightforward: just insert the alternate content inside the <canvas> element. Browsers that don't support <canvas> will ignore the container and render the fallback content inside it. Browsers that do support <canvas> will ignore the content inside the container, and just render the canvas normally.`


>`Required </canvas> tag`
`As a consequence of the way fallback is provided, unlike the <img> element, the <canvas> element requires the closing tag (</canvas>). If this tag is not present, the rest of the document would be considered the fallback content and wouldn't be displayed.`


`If fallback content is not needed, a simple <canvas id="foo" ...></canvas> is fully compatible with all browsers that support canvas at all.`

***IN ORDER TO LEARN HOW TO DRAW DIFFERENT KIND OF SHAPRES ON CANVAS VISIT THIS SITE: https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes#the_grid***

**Colors**
Up until now we have only seen methods of the drawing context. If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

![text](https://miro.medium.com/max/3524/1*72II7JJoLugWTsztSaBN8w.png)


**fillStyle** = color
Sets the style used when filling shapes.


**strokeStyle** = color
Sets the style for shapes' outlines.

`color is a string representing a CSS <color>, a gradient object, or a pattern object. We'll look at gradient and pattern objects later. By default, the stroke and fill color are set to black (CSS color value #000000).`


![cavas](https://www.webfx.com/blog/images/assets/images.sixrevisions.com/2010/10/03-01_html5_canvas_element_ld_img.png)

**Drawing text**

The canvas rendering context provides two methods to render text:

fillText(text, x, y [, maxWidth])

Fills a given text at the given (x,y) position. 

Optionally with a maximum width to draw.
strokeText(text, x, y [, maxWidth])


Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.


**Styling text**

In the examples above we are already making use of the font property to make the text a bit larger than the default size. There are some more properties which let you adjust the way the text gets displayed on the canvas:

font = value
The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.
textAlign = value
Text alignment setting. Possible values: start, end, left, right or center. The default value is start.
textBaseline = value
Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.
direction = value
Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.
These properties might be familiar to you, if you have worked with CSS before.