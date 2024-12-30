Sure! I've transformed your text into notes and added them into a markdown file. You can download it using the link below:

Download alignment_notes.md

Here's a preview of the notes:

```markdown
# Notes on Alignment Basics

## Horizontal Alignment
- Focus on horizontal alignment first; vertical alignment is more difficult and will be explored later.

## Text Alignment
- Aligning text within an HTML element is simple using the `text-align` CSS property.
- Example:
  ```css
  p {
      text-align: center;
  }
  ```
- Text alignment options: left, right, center, justify.
- Justify alignment spreads text so every line has the same width.
- Default alignment is left for left-to-right languages (e.g., English) and right for right-to-left languages (e.g., Arabic).

## HTML Element Alignment
- More complicated than text alignment.
- Involves the box model and document flow.

## HTML Element Center Alignment
- Set a width on the element and push its margins out to fill the remaining space of the parent element.
- Example HTML structure:
  ```html
  <div class="parent">
    <div class="child"></div>
  </div>
  ```
- CSS for parent element:
  ```css
  .parent {
    border: 4px solid red;
  }
  ```
- CSS for child element:
  ```css
  .child {
    width: 50%;
    padding: 20px;
    border: 4px solid green;
    margin: auto;
  }
  ```
- Works because the `div` element is a block-level element.
- To align an inline element like `img`, change it to a block-level element:
  ```html
  <div class="parent">
    <img src="photo.png" class="child">
  </div>
  ```
- CSS for `img` element:
  ```css
  .child {
    display: block;
    width: 50%;
    margin: auto;
  }
  ```
- Set only left and right margins to auto for more precise control:
  ```css
  .child {
    display: block;
    width: 50%;
    margin-left: auto;
    margin-right: auto;
  }
  ```

## HTML Element Left / Right Alignment
- Use the `float` property or the `position` property.
- `float` property example:
  ```html
  <div class="parent">
    <img src="photo.png" class="child"> Lorem ipsum dolor sit amet...
  </div>
  ```
- CSS for floating the image to the right:
  ```css
  .child {
    float: right;
  }
  ```
