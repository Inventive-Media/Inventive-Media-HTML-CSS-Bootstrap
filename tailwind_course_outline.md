# Build Custom Interfaces with Tailwind CSS

### A Utility-First Approach to Modern Web Design

---

## Slide 1: Title Slide

# Build Custom Interfaces with Tailwind CSS

### A Utility-First Approach to Modern Web Design

---

## Slide 2: What is Tailwind CSS?

- A **utility-first CSS framework** for rapidly building custom user interfaces.
- Style elements by applying pre-existing classes **directly in your HTML**.
- It does **not** ship with pre-designed components like Bootstrap (no `.card` or `.navbar`).
- You build fully custom designs from scratch by combining small, single-purpose classes.

---

## Slide 3: Adding Tailwind (CDN vs Locally)

### Two Ways to Get Started

| Method                     | Best For                                                                       | How to Use                                                                       |
| -------------------------- | ------------------------------------------------------------------------------ | -------------------------------------------------------------------------------- |
| **Play CDN**               | **Learning & Prototyping.** Directly in the browser, no installation required. | Add `<script src="https://cdn.tailwindcss.com"></script>` to your HTML `<head>`. |
| **Tailwind CLI (Locally)** | **Real Projects.** Compiles only the CSS you use for a tiny final file size.   | Use `npm install -D tailwindcss` and build your CSS via the command line.        |

> **Note:** The exact CDN link might change slightly over time. Always check the official website if it stops working!

---

## Slide 4: Utility Classes — Layout

### Controlling How Elements Behave

```html
<!-- A flexbox container that centers items vertically and spaces them out -->
<div class="flex items-center justify-between">
  <div>Left</div>
  <div>Right</div>
</div>
```

| Class                               | CSS Equivalent           |
| ----------------------------------- | ------------------------ | -------------- | ----- |
| `block`, `inline-block`, `hidden`   | `display: block          | inline-block   | none` |
| `flex`                              | `display: flex`          |
| `flex-col`, `flex-row`              | `flex-direction: column  | row`           |
| `items-center`                      | `align-items: center`    |
| `justify-center`, `justify-between` | `justify-content: center | space-between` |

---

## Slide 5: Utility Classes — Spacing

### Margin and Padding

```html
<!-- Padding on all sides, margin on top and bottom -->
<div class="p-4 my-6 mx-auto">Content here</div>
```

- **Prefix:** `p` (Padding) or `m` (Margin)
- **Direction:** `t` (top), `b` (bottom), `l` (left), `r` (right), `x` (horizontal), `y` (vertical)
- **Size:** `0`, `1`, `2`, `4`, `8`, etc. (1 unit = 0.25rem = 4px)
- **Center auto:** `mx-auto` (Centers block elements horizontally)

---

## Slide 6: Utility Classes — Typography

### Sizing, Weight, and Color

```html
<h1 class="text-3xl font-bold text-blue-600 text-center">Main Heading</h1>
<p class="text-base text-gray-700 italic">Some description text.</p>
```

| Category        | Tailwind Classes                                            |
| --------------- | ----------------------------------------------------------- |
| **Font Size**   | `text-sm`, `text-base`, `text-xl`, `text-3xl`               |
| **Font Weight** | `font-light`, `font-normal`, `font-semibold`, `font-bold`   |
| **Text Color**  | `text-black`, `text-white`, `text-blue-500`, `text-red-700` |
| **Alignment**   | `text-left`, `text-center`, `text-right`                    |

---

## Slide 7: Creating Responsive Designs

### The Mobile-First Approach

Tailwind uses responsive prefixes to apply styles only at specific screen widths and above.

```html
<!-- 1 column on mobile, 2 columns on tablet, 3 columns on desktop -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">...</div>
```

| Prefix   | Min Width | Target Device                   |
| -------- | --------- | ------------------------------- |
| _(none)_ | 0px       | Mobile (default starting point) |
| `sm:`    | 640px     | Small tablets                   |
| `md:`    | 768px     | Tablets                         |
| `lg:`    | 1024px    | Laptops / Desktops              |

---

## Slide 8: Styling Components — Buttons

### Building a Button from Scratch

Unlike Bootstrap's `.btn`, you combine utilities to create your own button.

```html
<!-- A primary blue button with hover effects -->
<button
  class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-lg shadow-md transition-colors"
>
  Click Me
</button>
```

- **Background:** `bg-blue-500`
- **Interactivity:** `hover:bg-blue-700` (Changes color on hover)
- **Typography:** `text-white font-bold`
- **Spacing:** `py-2 px-4`
- **Borders & Shadows:** `rounded-lg shadow-md`

---

## Slide 9: Styling Components — Cards

### Building a Simple Card Profile

```html
<div
  class="max-w-sm mx-auto bg-white border border-gray-200 rounded-xl shadow-lg overflow-hidden"
>
  <img class="w-full h-48 object-cover" src="image.jpg" alt="Profile" />

  <div class="p-6">
    <h2 class="text-xl font-bold text-gray-900 mb-2">John Doe</h2>
    <p class="text-gray-600 text-base">
      Web Developer specializing in Tailwind CSS.
    </p>
  </div>
</div>
```

- **Container:** `max-w-sm mx-auto bg-white border rounded-xl shadow-lg`
- **Image handling:** `w-full h-48 object-cover` to cleanly crop the image
- **Internal spacing:** `p-6` around the text content

---

## Slide 10: Resources & Next Steps

| Resource                                          | Description                                    |
| ------------------------------------------------- | ---------------------------------------------- |
| [Tailwind CSS Docs](https://tailwindcss.com/docs) | The official documentation—your best friend!   |
| [Tailwind Play](https://play.tailwindcss.com)     | Browser-based code playground to test classes. |

---
