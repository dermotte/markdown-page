# Markdown Page

A simple web application that loads and renders Markdown files as HTML pages using Bootstrap 5.3 and Showdown.js.

## Features

- **Dynamic Content Loading** - Load different markdown files via URL parameters (e.g., `?d=data/about.md`)
- **Bootstrap Integration** - Responsive layout using Bootstrap 5.3 CSS framework
- **Markdown Rendering** - Converts Markdown to HTML using Showdown.js with table support
- **Loading State** - Shows a spinner while content is being fetched

## Project Structure

```
markdown-page/
├── index.html          # Main HTML file with JavaScript logic
├── css/
│   └── style.css       # Custom CSS styles
├── data/               # Markdown content files
│   ├── index.md        # Sample home page content
│   └── about.md        # Sample about page
└── js/                 # Additional JavaScript files
```

## Usage

1. **Open in Browser** - Simply open `index.html` in your web browser
2. **Load Different Content** - Use the `d` URL parameter to load different markdown files:
   - Home page: `index.html`
   - About page: `index.html?d=data/about.md`

## Markdown File Format

Create new pages by adding `.md` files to the `data/` directory. The application will automatically render them.

Example markdown file, find more in the data directory.:

```markdown
# Page Title

Your content here with **bold**, *italic*, and [links](http://example.com).
```

## How to adapt it to your needs

### Changing the Framework

The project currently uses Bootstrap 5.3 with a theme from [Bootswatch](https://cdnjs.com/libraries/bootswatch). To change the framework:

1. Open `index.html` in the root directory
2. Look for the `<head>` section
3. Replace the Bootstrap CSS link with your preferred framework:
   - **Tailwind CSS**: `<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">`
   - **Foundation**: `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/foundation-sites@6.7.5/dist/css/foundation.min.css">`
   - **Semantic UI**: `<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/semantic-ui-css@2.5.0/semantic.min.css">`
4. Update the HTML structure in the `<body>` section to match your framework's class names

### Customizing the CSS

All custom styles are located in `css/style.css`. You can modify this file to change the appearance of your Markdown pages.

**Current custom styles include:**

| Property | Current Value | Description |
|----------|---------------|-------------|
| `padding` | `3pt` | Table cell padding |
| `border-width` | `1pt` | Table border thickness |
| `margin-bottom` | `12pt` | Space below tables |
| `margin-top` | `6pt` | Space above tables |

**Common customizations:**

1. **Typography**
   ```css
   body {
       font-family: 'Arial', sans-serif;  /* Change font family */
       font-size: 16px;                  /* Adjust base font size */
       line-height: 1.6;                 /* Improve readability */
   }
   ```

2. **Colors**
   ```css
   body {
       background-color: #f5f5f5;  /* Light background */
       color: #333333;            /* Dark text */
   }
   h1, h2, h3 {
       color: #007bff;  /* Blue headings */
   }
   a {
       color: #0056b3;  /* Darker links */
   }
   a:hover {
       color: #003d80;  /* Darker on hover */
   }
   ```

3. **Container Width**
   ```css
   .container {
       max-width: 800px;  /* Wider content area */
   }
   ```

4. **Markdown Content Styling**
   ```css
   /* Code blocks */
   pre {
       background-color: #f4f4f4;
       padding: 15px;
       border-radius: 5px;
       overflow-x: auto;
   }
   
   /* Blockquotes */
   blockquote {
       border-left: 4px solid #007bff;
       margin: 0;
       padding: 10px 20px;
       background-color: #f8f9fa;
   }
   
   /* Horizontal rules */
   hr {
       border: 0;
       border-top: 2px solid #dee2e6;
       margin: 20px 0;
   }
   ```

5. **Responsive Adjustments**
   ```css
   @media (max-width: 768px) {
       body {
           font-size: 14px;
       }
       .container {
           padding: 10px;
       }
   }
   ```

**Tips for editing CSS:**
- Use specific selectors to override Bootstrap styles when needed
- Test changes in different browsers
- Consider using browser developer tools (F12) to inspect elements and test styles
- Keep your custom CSS separate from framework CSS for easier updates
- Use CSS variables for consistent theming: `:root { --primary-color: #007bff; }`

**To load a custom CSS file:**
1. Place your CSS file in the `css/` directory
2. Add a `<link>` tag in `index.html` `<head>` section:
   ```html
   <link href="css/custom.css" rel="stylesheet">
   ```

## Technology Stack

- HTML5
- CSS3 (Bootstrap 5.3)
- JavaScript (ES6+)
- Showdown.js 2.1.0 - Markdown to HTML converter
- Phosphor Icons - Icon library

## License

This project is open source and available under the MIT License.
