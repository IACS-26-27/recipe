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

- A title for your recipe (`<h1>`)
- A short introduction in paragraphs (`<p>`)
- At least one image (`<img>`) with `alt` text describing it
- An **Ingredients** section (`<h2>`) with an unordered list (`<ul>`)
- An **Instructions** section (`<h2>`) with an ordered list (`<ol>`)
- At least one subheading (`<h3>`) — for example, "For the Sauce" and
  "For the Dough," or "Before You Start"
- At least one extra section of your choice, such as **Tips**, **Serving
  Suggestions**, or **Why This Recipe Works**
- A citations page (`citations.html`, already linked in your footer) crediting any
  images or other sources you used and acknowledging any AI use.

### CSS Design:

Your stylesheet should customize:

- **Color:** A color scheme of at least 3 colors that fits your recipe, with
  text that is easy to read against its background.
- **Fonts:** At least one custom font from [Google Fonts](https://fonts.google.com/),
  and font sizes that make it clear what is most important on the page.
- **Element selectors:** Rules that change how your elements look
  (for example `h2 { ... }`, `li { ... }`).
- **Classes:** At least one class (for example `.tip` or `.warning`) that
  styles _some_ elements differently from others of the same type.
- **The box model:** `padding`, `margin`, and `border` to group related
  content and give your page room to breathe, plus a `width` or `max-width`
  so your text isn't stretched across the whole screen.

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

- Use a descendant selector (like `ol li` or `.tip p`) to style elements only
  when they are inside something else.
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

<table border="1">
  <tr>
    <th>Criteria</th>
    <th>1 - Beginning</th>
    <th>2 - Developing</th>
    <th>3 - Proficient</th>
    <th>4 - Mastery</th>
  </tr>
  <tr>
    <th>Recipe Structure</th>
    <td><!-- structure | 1 --></td>
    <td><!-- structure | 2 --></td>
    <td><ul>
          <li>The recipe includes:
            <ul>
              <li>Headings</li>
              <li>Sections (such as <code>div</code>, <code>main</code>, or <code>section</code>)</li>
              <li>Lists</li>
            </ul>
          </li>
        </ul></td>
    <td><ul>
          <li>Nuanced formatting, e.g. the amount, unit, and ingredient in each ingredient are styled distinctly.</li>
        </ul></td>
  </tr>
  <tr>
    <th>CSS Design</th>
    <td><!-- design | 1 --></td>
    <td><!-- design | 2 --></td>
    <td><ul>
          <li>CSS is used to customize:
            <ul>
              <li>Fonts</li>
              <li>Colors</li>
              <li>Padding and margins</li>
            </ul>
          </li>
        </ul></td>
    <td><ul>
          <li>The recipe layout is highly intentional and carefully crafted.</li>
        </ul></td>
  </tr>
  <tr>
    <th>Organization & Process</th>
    <td><!-- process | 1 --></td>
    <td><!-- process | 2 --></td>
    <td><!-- process | 3 --></td>
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
    <th>4 - Excellent</th>
  </tr>
  <tr>
    <th>CSS Rules & Selectors</th>
    <td><!-- Rules | 1 --></td>
    <td><!-- Rules | 2 --></td>
    <td><ul><li>Explains the parts of a CSS rule (selector, property, value) and what an element selector does.</li></ul></td>
    <td><ul>
          <li>Explains the difference between an element selector and a class selector, and when to use each.</li>
          <li>Predicts which elements a given selector will style.</li>
        </ul></td>
  </tr>
  <tr>
    <th>The Box Model</th>
    <td><!-- BoxModel | 1 --></td>
    <td><!-- BoxModel | 2 --></td>
    <td><ul><li>Identifies content, padding, border, and margin in a diagram or on a page.</li></ul></td>
    <td><ul>
          <li>Explains when to use padding versus margin to create a specific effect.</li>
        </ul></td>
  </tr>
  <tr>
    <th>Design Choices</th>
    <td><!-- Design | 1 --></td>
    <td><!-- Design | 2 --></td>
    <td><ul><li>Describes the color and font choices made on the website.</li></ul></td>
    <td><ul>
          <li>Explains how color, typography, and spacing choices support the mood of the recipe and make it easy to read.</li>
        </ul></td>
  </tr>
  <tr>
    <th>The Cascade (Honors)</th>
    <td><!-- Cascade | 1 --></td>
    <td><!-- Cascade | 2 --></td>
    <td><ul><li>Explains what happens when two rules style the same element.</li></ul></td>
    <td><ul>
          <li>Explains how inheritance and specificity decide which rule wins.</li>
        </ul></td>
  </tr>
</table>
