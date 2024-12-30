
# Building a Responsive Website with Bootstrap Grid System

## Responsive Design and Bootstrap Grid

Building a website using responsive design requires a responsive grid and responsive breakpoints. Bootstrap provides both of these as part of its library. 

The **Bootstrap grid system** helps to create web page layouts through a series of rows and columns that house content. 

### Key Features of the Bootstrap Grid System:
- **12-column grid**: It can be fluid or fixed.
- **Container**: The root element of the grid, used to pad and align content. Its width is determined based on the current responsive breakpoint.
- **Rows and Columns**: Rows are added inside the container, and columns are added within rows.

## Demonstrating Bootstrap Grid with Little Lemon's Website

### Adding Columns
In the web page example, two columns were added to a row. By default, Bootstrap sets the two columns to span **six column spaces each**.

To customize column widths:
- **Shrink the price column** to 4 spaces: Add the suffix `-4` to the `col` CSS class above the prices heading.
- **Expand the menu column** to 8 spaces: Add the suffix `-8` to the `col` CSS class above the menu heading.

### Responsive Breakpoints
Bootstrap enables configuring content to use different layouts based on the device using **breakpoint-specific CSS rules**.

#### Example: Stacking Content on Mobile and Side-by-Side on Desktop
1. **For mobile devices**: 
   - Set columns to use **12 spaces each** by adding `-12` as a suffix to the `col` rule for both columns.
2. **For desktop devices**:
   - Set columns to **6 spaces each** by adding a `col-lg` rule and suffix `-6` for the column sizes.

### Testing the Layout
1. Save the file and open it in a web browser.
2. Use developer tools (press `F12`):
   - Click the **mobile phone/tablet button** in the top left corner to enable device mode.
   - Simulate viewing the website on a mobile phone. Observe how content stacks vertically on smaller devices.

### Advantages of Bootstrap's Grid System
- **Responsive Layouts**: Content adjusts to different devices seamlessly.
- **Efficiency**: Eliminates the need to develop separate layouts for various devices.
- **Powerful and Versatile**: Suitable for most development needs.

The Bootstrap grid system ensures that your website is both responsive and efficient, saving development time and providing a consistent user experience.
