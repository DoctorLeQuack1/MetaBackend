# Notes on Creating a Simple Bootstrap Webpage

## Introduction
- Designing a website involves positioning UI elements and menus on the page.
- Bootstrap is a collection of pre-written CSS and JavaScript code that helps create websites quickly.

## Setting Up the Layout
1. **Container Elements**:
   - Add a container element using the `container` CSS class provided by Bootstrap.
   - Example:
     ```html
     <div class="container"></div>
     ```

2. **Row Elements**:
   - Add a row for the contents using the `row` CSS class.
   - Example:
     ```html
     <div class="row"></div>
     ```

3. **Column Elements**:
   - Add columns using the `col` CSS class.
   - Example:
     ```html
     <div class="col"></div>
     ```

## Adding Content
1. **Naming Columns**:
   - Use heading tags to name the columns.
   - Example:
     ```html
     <div class="col">
       <h1>Our Menu</h1>
     </div>
     <div class="col">
       <h2>Prices</h2>
     </div>
     ```

2. **Adding Dishes**:
   - Add dish names, ingredients, and images.
   - Example:
     ```html
     <div class="col">
       <h2>Falafel</h2>
       <p>Chickpea, herbs, and spices</p>
       <img src="falafel.jpeg" class="img-fluid" alt="Falafel">
     </div>
     <div class="col">
       <h2>Pasta Salad</h2>
       <p>Lettuce, vegetables, and mozzarella</p>
       <img src="salad.jpeg" class="img-fluid" alt="Pasta Salad">
     </div>
     ```

## Adding a Price Table
1. **Table Structure**:
   - Add a table using the `table` CSS class.
   - Example:
     ```html
     <table class="table">
       <tr>
         <td>Falafel</td>
         <td>$12</td>
       </tr>
       <tr>
         <td>Pasta Salad</td>
         <td>$10</td>
       </tr>
     </table>
     ```

## Conclusion
- Save the file and preview the webpage.
- The dishes are displayed in columns, and the images are sized correctly.
- The table structure displays using Bootstrap's table style.

