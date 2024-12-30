
# Notes on CSS and HTML Elements

## Document Flow
- The web browser's normal way of calculating the position of HTML elements on the screen is called document flow.
- HTML elements are organized into two categories: block and inline elements.

## Block Level Elements
- Occupy the full horizontal width of their parent element and the vertical height of their content.
- Have a new line before and after.
- Stack on top of each other like a stack of boxes.
- Examples: div, form, heading tags.

## Inline Elements
- Occupy only the width and height of their content.
- Do not appear on a new line.
- Can form a row of elements.
- Examples: anchor, image, input, label, bold, italics, emphasis, span.

## Example Demonstration
1. Open Visual Studio Code.
2. Create an HTML file with div and span elements.
3. Notice that div elements contain block-level content and span elements contain inline content.
4. Change a span element to a div element to see it move to a new line.
5. Use the CSS display property to change elements from block to inline and vice versa.

## CSS Display Property
- Use `display: inline;` to change a block element to an inline element.
- Use `display: block;` to change an inline element to a block element.

## Conclusion
- Block elements begin on a new line and take up the full width of the page.
- Inline elements work within the flow of surrounding content rather than breaking onto their own line.
