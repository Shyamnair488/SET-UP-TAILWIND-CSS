Here's the corrected and complete version of your `README.md` file for setting up Tailwind CSS in your project:

```markdown
# Tailwind CSS Setup Guide for Your Project

This guide will help you set up a project with Tailwind CSS for building your website. Follow these steps to get started.

## Prerequisites

Ensure that **Node.js** is installed on your system. If not, download and install it from the [official Node.js website](https://nodejs.org/).

---

## Steps to Set Up the Project

### 1. Install Node.js

If Node.js isn't already installed, install it from the [official website](https://nodejs.org/).

---

### 2. Create Project Directory Structure

Set up your project folder as follows:

```plaintext
your-project/
├── dist/
│   └── index.html
└── src/
    └── input.css
```

---

### 3. Install Tailwind CSS

In the terminal (VS Code or any terminal you use), run the following commands to install Tailwind CSS and initialize it:

```bash
npm install -D tailwindcss
npx tailwindcss init
```

This will install Tailwind CSS and generate a `tailwind.config.js` file in your project.

---

### 4. Create `input.css` File

Create a new file called `input.css` inside the `src/` folder. Add the following lines to `input.css`:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

If you encounter any errors, press `Ctrl + ,` (comma) in VS Code, search for "unknown", and choose to ignore the error.

---

### 5. Install VS Code Extensions

To enhance your development experience, install the following VS Code extensions:

- **Tailwind CSS IntelliSense**
- **Tailwind CSS IntelliSense with Hex Colors**

---

### 6. Link Tailwind CSS in `index.html`

In your `dist/index.html` file, add the following script tag inside the `<head>` section:

```html
<script src="https://cdn.tailwindcss.com"></script>
```

---

### 7. Update `tailwind.config.js`

Now, open the `tailwind.config.js` file and update it with the following configuration:

```javascript
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./dist/index.html"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

---

### 8. Generate the Tailwind CSS File

Run the following command in the terminal to generate the compiled CSS file:

```bash
npx tailwindcss -i ./src/input.css -o ./dist/style.css
```

This will compile the Tailwind CSS into a `style.css` file in the `dist/` folder.

---

### 9. Watch for Real-Time Updates

To automatically update your `style.css` file whenever you make changes to `input.css`, run the following command:

```bash
npx tailwindcss -i ./src/input.css -o ./dist/style.css --watch
```

This will watch for changes and recompile the CSS in real-time.

---

### 10. Update `tailwind.config.js` for Multiple HTML Files

If you have multiple HTML files in the `dist/` folder, update the `content` section in your `tailwind.config.js` file to:

```javascript
module.exports = {
  content: ["./dist/*.html"],  // Update for multiple HTML files
  theme: {
    extend: {},
  },
  plugins: [],
}
```

---

### Additional Resources

For more detailed information, refer to the official [Tailwind CSS Documentation](https://tailwindcss.com/docs).

---

### Next Steps

You can now start building your website by adding Tailwind CSS classes to your HTML files.

Make sure to keep the `npx tailwindcss -i ./src/input.css -o ./dist/style.css --watch` command running in your terminal to automatically update the CSS.

Happy coding! 🚀
```

### Key Changes and Fixes:
- Corrected some formatting issues.
- Added missing details like the `src/input.css` file under directory structure.
- Fixed code block and command formatting to be consistent throughout the file.
- Updated each step for clarity and structure.

You can copy and paste this into your `README.md` file, and it will render correctly in Markdown viewers like GitHub. Let me know if you need further adjustments!