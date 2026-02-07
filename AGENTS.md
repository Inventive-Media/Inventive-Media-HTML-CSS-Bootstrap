# Project Guidelines

## Code Style

### HTML

- **Indentation:** Use 2 spaces for indentation.
- **Formatting:**
  - Use lowercase for all tags and attributes.
  - Wrap attribute values in double quotes.
  - Use self-closing tags for void elements (e.g., `<meta />`, `<br />`, `<img />`).
- **Lesson Structure:**
  - Place lesson-specific styles in a `<style>` block within the `<head>`.
  - Use `.code-block` div with HTML entities (e.g., `&lt;`) for displaying code snippets.
  - Use `.example-output` div for live rendering of examples.
  - Include "Previous" and "Next" navigation links at the bottom of the `<body>`.

### CSS

- **Indentation:** Use 2 spaces.
- **Naming:** Use `kebab-case` for classes and IDs (e.g., `.section-title`, `#main-content`).
- **Formatting:**
  - Opening brace on the same line as the selector.
  - One property per line.
  - Space after the colon in properties.

## Architecture

The project is organized into daily modules, consisting primarily of static HTML files.

- **`day-1/`**: HTML Basics.
- **`day-2/`**: CSS Basics.
- **`day-3/`**: Bootstrap & Layouts (includes local `css/` and `js/` folders for library files).

## Build and Test

- **Run:** There are no build steps. Open `.html` files directly in a web browser to view them.
- **Dependencies:** `day-3` relies on local Bootstrap files located in `day-3/css/` and `day-3/js/`.

## Project Conventions

- **File Naming:**
  - Use `snake_case` (e.g., `block_elements.html`).
  - For ordered lessons (Day 2+), use numbered prefixes (e.g., `01_setup.html`, `12_grid.html`).

## Comments

Comments are used extensively for educational purposes and structuring the files.

### HTML Comments

Use multi-line block comments to separate major sections and explain concepts.

- **Structure:**
  ```html
  <!-- 
    SECTION [Number]: [TITLE]
    [Brief description or instruction about the concept being demonstrated]
  -->
  ```
- **Example:**
  ```html
  <!-- 
    SECTION 1: HEADINGS
    Headings are used to define the structure and hierarchy of content.
    h1 is the most important, h6 is the least important.
  -->
  ```

### CSS Comments

Use comments to group styles and explain specific properties.

- **Section Headers:** Use dashed lines to separate logical groups of styles.
  ```css
  /* --- TYPOGRAPHY --- */
  ```
- **Explanations:** Use inline or block comments to explain _why_ a property is used.
  ```css
  /* Ensures the container centers its children */
  display: flex;
  justify-content: center;
  ```
