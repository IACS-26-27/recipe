# Recipe Project

For an overview of how to use GitHub Codespaces, see my
[Sandbox Overview](SandboxOverview.md)

To see your page, open the terminal and type `npm start`.

## Task

Build a one-page recipe website, then use CSS to design how it looks.

Your recipe can be **real** (your grandmother's empanadas, the perfect grilled
cheese, a smoothie you invented) or **metaphorical** ("The Recipe for Becoming
a Great Snowboarder," "How to Cook Up the Perfect Snow Day," "A Recipe for
Surviving Freshman Year").

## Why a Recipe?

Recipes are one of the oldest kinds of structured writing. Every recipe has
the same basic parts — a title, a little introduction, a list of ingredients,
and numbered steps — but if you look at ten cookbooks or food blogs, you'll
see ten completely different designs.

That makes a recipe perfect for learning CSS. You'll write the structure in
HTML, and then use CSS to decide what that structure _looks like_: its colors,
its fonts, and the spacing that makes it easy (and fun) to read.

## A Note on AI

**Important:** While Generative AI tools such as ChatGPT or Claude.ai can be
useful for tasks like this, their results often lack creativity and feel
lifeless. **DO NOT** use AI to generate your entire webpage or stylesheet for
this assignment — this is considered cheating.

However, you **may** use AI to assist with individual elements, but you must
credit it wherever applicable. For example, if you asked AI to help you come
up with a list of ingredients for a metaphorical recipe, you would need to
include a comment in your code to credit the AI:

```html
<!-- AI-assisted content: ingredient ideas brainstormed with ChatGPT -->
```

## Required Components

### HTML Structure:

- A title for your recipe (`<h1>`), section headings (`<h2>`), and at least
  one subheading (`<h3>`) — for example, "For the Sauce" and "For the Dough,"
  or "Before You Start"
- A short introduction in paragraphs (`<p>`)
- An **Ingredients** list (`<ul>`) and an **Instructions** list (`<ol>`)
- At least one image (`<img>`) with `alt` text describing it
- At least one extra section of your choice, such as **Tips**, **Serving
  Suggestions**, or **Why This Recipe Works**
- **Semantic groupings:** use `<header>`, `<main>`, and `<footer>` for the
  big parts of the page, and wrap each part of your recipe (introduction,
  ingredients, instructions, extra section) in its own `<section>` or `<div>`
- A citations page (`citations.html`, already linked in your footer) crediting any
  images or other sources you used and acknowledging any AI use.

### What to Style:

Your stylesheet should have rules for each of these:

- **The page** (`body`): background color, text color, and your main font
- **Headings** (`h1`, `h2`, `h3`): a heading font, colors, and sizes that make
  it clear what is most important
- **Text** (`p`, `li`): a readable font size and `line-height`
- **Your sections:** `padding`, `margin`, and a `border` or background color
  so each part of the recipe is clearly grouped
- **Images:** a size that fits nicely on the page
- **Header and footer**, including the link to your citations page

### CSS Requirements:

- **Color:** A color scheme of at least 3 colors that fits your recipe, with
  text that is easy to read against its background.
- **Fonts:** At least one custom font from [Google Fonts](https://fonts.google.com/).
- **The typography triangle:** Readable text comes from balancing three things:
  - `font-size` — how big the letters are
  - `line-height` — how much space is between the lines
  - `max-width` — how long each line can get

  Change one and you'll usually need to adjust the others.
- **Selectors:** Element selectors (`h2 { ... }`), at least one class
  (`.tip { ... }`) that styles _some_ elements differently from others of the
  same type, and at least one descendant selector (`.tip p { ... }`) that
  styles elements only when they are inside something else.
- **The box model:** `padding`, `margin`, and `border` to group related
  content and give your page room to breathe.
- **Organization:** Your `styles.css` is organized into sections with
  comments explaining what each part styles.

**No layout tools yet!** For this project, your page should flow from top to
bottom. Do not use `display: flex`, `display: grid`, or `position`.
We'll get to those soon. That means you generally won't be able to put items
side-by-side in this project (unless you use `float`).

### Honors Components (in addition to main components):

- Store your color scheme in CSS variables (`--main-color: ...;`) and use
  them throughout your stylesheet. For example:

  ```css
  :root {
    --theme-color: #0033a0;
  }
  h1 {
    color: var(--theme-color);
  }
  ```

- **Advanced typography:** pair a heading font with a body font, and use at
  least three of these to fine-tune your text:
  - `font-weight` (using more than one weight of a font)
  - `letter-spacing`
  - `text-transform` (for example, all-caps headings)
  - `font-variant: small-caps`
  - `font-variant-numeric: diagonal-fractions` (makes 1/2 look like ½)
  - `text-align` and `text-indent`
- Customize list markers (bullets and numbers) using `list-style` or `::marker`.
- Use a pseudo-element (`::before` or `::after`) to add a custom marker to at least one item.
- Use a "recipe info" box (prep time, cook time, servings — or the
  metaphorical equivalent) styled with a class.

## Resources

- [Mr. H's YouTube Tutorials](https://www.youtube.com/playlist?list=PLMEapm-6E2Mg) 
- [Validity Checker](https://validator.w3.org/nu/) _(ignore character encoding warnings)_
- [W3Schools CSS Tutorial](https://www.w3schools.com/css/default.asp)
- [MDN: CSS Selectors](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Basic_selectors)
- [MDN: The Box Model](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Styling_basics/Box_model)
<!-- TODO: add typography triangle resource link(s) -->

### Color & Font Resources

- [Coolors](https://coolors.co/) — generate color schemes, or pull one from an image
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) — make sure your text is readable
- [Google Fonts](https://fonts.google.com/) — pick a font and copy its `<link>` tag into your `<head>`

### Honors Resources

- [CSS Custom Properties (Variables) - W3Schools](https://www.w3schools.com/css/css3_variables.asp)
- [Styling Lists - MDN](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Text_styling/Styling_lists)
- [The `::marker` pseudo-element - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/::marker)
- [The `::before` and `::after` pseudo-elements - W3Schools](https://www.w3schools.com/css/css_pseudo_elements.asp)

# Recipe Project Rubric

Grading will happen in two phases:

1. You will get a "Digital Creation" grade based on the quality of your published website.

2. You will get a "Content" grade based on your in-class write-up explaining your code and design decisions.

## Published Website Rubric

Starred items (\*) are for honors students.

<table border="1">
  <tr>
    <th>Criteria</th>
    <th>1 - Beginning</th>
    <th>2 - Developing</th>
    <th>3 - Proficient</th>
    <th>4 - Mastery</th>
  </tr>
  <tr>
    <th>CSS</th>
    <td><!-- css | 1 --></td>
    <td><!-- css | 2 --></td>
    <td><ul>
          <li>CSS is used to customize:
            <ul>
              <li>Fonts</li>
              <li>Colors</li>
              <li>Padding and margins</li>
            </ul>
          </li>
          <li>Font size, line height, and width work together so text is easy to read.</li>
        </ul></td>
    <td><ul>
          <li>The recipe layout is highly intentional and carefully crafted.</li>
          <li>Uses CSS variables and advanced typography settings.*</li>
        </ul></td>
  </tr>
  <tr>
    <th>HTML</th>
    <td><!-- html | 1 --></td>
    <td><!-- html | 2 --></td>
    <td><ul>
          <li>The recipe includes:
            <ul>
              <li>Headings</li>
              <li>Sections (such as <code>header</code>, <code>main</code>, <code>section</code>, <code>div</code>, <code>footer</code>)</li>
              <li>Lists</li>
            </ul>
          </li>
        </ul></td>
    <td><ul>
          <li>Nuanced formatting, e.g. the amount, unit, and ingredient in each ingredient are marked up and styled distinctly.</li>
          <li>Includes a "recipe info" box styled with a class.*</li>
        </ul></td>
  </tr>
  <tr>
    <th>Process</th>
    <td><!-- process | 1 --></td>
    <td><!-- process | 2 --></td>
    <td><ul>
          <li>The site passes validation with minor issues.</li>
        </ul></td>
    <td><ul>
          <li>CSS is organized into sections with comments.</li>
          <li>A steady log of commit messages shows progress over time.</li>
        </ul></td>
  </tr>
</table>

## In-Class Write-Up Rubric (Content Strand)

This will be an assessment based on an in-class write-up you will do with questions you will not know ahead of time.

<table border="1">
  <tr>
    <th>Criteria</th>
    <th>1 - Beginning</th>
    <th>2 - Developing</th>
    <th>3 - Proficient</th>
    <th>4 - Mastery</th>
  </tr>
  <tr>
    <th>CSS Properties & Values</th>
    <td><!-- properties | 1 --></td>
    <td><!-- properties | 2 --></td>
    <td><ul><li>Identifies the selector, property, and value in a CSS rule, and explains what common properties (such as <code>color</code>, <code>font-size</code>, <code>padding</code>, <code>margin</code>) do.</li></ul></td>
    <td><ul>
          <li>Predicts how changing a value will change the page, and chooses properties and values to create a described effect.</li>
        </ul></td>
  </tr>
  <tr>
    <th>Selectors</th>
    <td><!-- selectors | 1 --></td>
    <td><!-- selectors | 2 --></td>
    <td><ul><li>Explains which elements an element selector (<code>li</code>) and a class selector (<code>.tip</code>) will style.</li></ul></td>
    <td><ul>
          <li>Predicts which elements a descendant (nested) selector like <code>.tip p</code> will style, and writes a selector to target a described element.</li>
        </ul></td>
  </tr>
</table>
