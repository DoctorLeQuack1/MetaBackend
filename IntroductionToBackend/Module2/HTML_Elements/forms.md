# HTML Forms Notes

## Introduction

*   Online shopping relies heavily on HTML forms.
*   Forms are used for various online interactions, including logins.

## How Forms Work

*   User input in a form generates an HTTP request sent to the server.

## Creating a Form

*   Forms are defined using the `<form>` tag.
*   **`action` attribute (optional):** Specifies the URL/path where the form data is submitted. If not specified, the form submits to the current page's path.
*   **`method` attribute:** Specifies the HTTP method used for submission (GET or POST).
    *   **GET:** Retrieves information from the server.
    *   **POST:** Sends data to the server.

## Form Fields (Input Types)

*   Fields are created using the `<input>` tag (self-closing).

### Text Field

*   `type="text"`: Creates a single-line text input field (e.g., for usernames).
*   `<label>` tag: Adds a descriptive label above the input field for better user experience. Example: `<label for="username">Username:</label><input type="text" id="username">`

### Password Field

*   `type="password"`: Creates a masked input field for passwords.

### Submit Button

*   `type="submit"`: Creates a button that submits the form data to the server.

## Form Structure Summary

1.  Start with the `<form>` tag, including the `method` attribute.
2.  Use `<label>` tags for input field descriptions.
3.  Use `type="text"` for text inputs.
4.  Use `type="password"` for password inputs.
5.  Use `type="submit"` to create a submit button.

## Other Input Types

*   **Checkboxes:**
    *   `type="checkbox"`: Creates selectable boxes (multiple selections allowed).
    *   `name` and `value` attributes configure how data is sent (covered in later material).
*   **Radio Buttons:**
    *   `type="radio"`: Creates a group of selectable buttons where only one can be selected at a time. Selecting one unselects others in the group.
*   **Other Input Types:**
    *   `type="number"`: For numeric input.
    *   `type="email"`: For email address input (with basic validation).
    *   `type="file"`: For file uploads.

## Multi-line Text Input

*   Not created with the `<input>` tag.
*   Uses the `<textarea>` tag for multi-line text input. This allows for larger text input areas.

## Example (Illustrative)

```html
<form method="POST" action="/submit_form">
  <label for="username">Username:</label><br>
  <input type="text" id="username" name="username"><br><br>

  <label for="password">Password:</label><br>
  <input type="password" id="password" name="password"><br><br>

  <input type="submit" value="Submit">
</form>