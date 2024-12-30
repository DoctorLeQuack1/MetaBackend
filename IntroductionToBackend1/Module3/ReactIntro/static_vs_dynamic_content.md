
# Static vs Dynamic Content and the Role of Servers

When you shop online, websites often provide personalized recommendations. These recommendations differ for each user. This differentiation is possible due to the adaptation of websites to different user profiles.

## Static vs Dynamic Content

- **Static Content**: Files transferred as they are stored on the web server (e.g., videos or images).
- **Dynamic Content**: Generated when the HTTP request is made, often based on user input or the current date.

### Key Differences

| Static Content             | Dynamic Content                   |
|----------------------------|-----------------------------------|
| Pre-stored on the server    | Generated during the HTTP request |
| Faster to send              | Takes longer due to processing   |

## Role of Web and Application Servers

1. **Web Server**: Handles HTTP requests and serves content to the browser.
2. **Application Server (Back-end)**: Generates dynamic content and performs complex processing.

### Examples

- Watching a video: Static content is sent by the web server.
- Logging in to a course: Dynamic content is processed by the application server.

### How Application Servers Work

- **Responsibilities**:
  - Run application logic.
  - Communicate with databases.
  - Check permissions.
- **Specialized Servers**:
  - Purpose-specific application servers exist for tasks like music streaming or blogging.

## Caching: Improving Performance

Dynamic content generation can be slow, which poses challenges for high-traffic websites. **Caching** addresses this:

1. **First Request**:
   - Web server checks for cached content.
   - If not cached, it requests from the application server.
   - Saves the dynamic content in the cache and sends it to the browser.

2. **Subsequent Requests**:
   - Cached content is sent immediately by the web server.
   - Periodic updates refresh the cache with the latest content.

## Conclusion

- Understand the differences between static and dynamic content.
- Recognize the roles of web and application servers.
- Identify static and dynamic content on the websites you visit.
