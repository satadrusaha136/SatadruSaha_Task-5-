# Complete CSS Documentation

## Responsive Laundry Website — TuteDude Task 5

This document explains the CSS properties used in the responsive laundry website, including the navbar, hero section, image, button, and media queries.

---

# 1. Universal Selector and Box Sizing

```css
* {
    box-sizing: border-box;
}
```

### `*` — Universal Selector

The universal selector selects every HTML element on the page.

For example:

```css
* {
    color: blue;
}
```

This applies blue text color to all elements.

### `box-sizing`

The `box-sizing` property controls how the browser calculates an element's width and height.

### `border-box`

When `box-sizing: border-box` is used, the declared width and height include the element's content, padding, and border.

Example:

```css
div {
    width: 300px;
    padding: 20px;
    border: 5px solid black;
    box-sizing: border-box;
}
```

The total width remains 300px because the padding and border are included.

---

# 2. HTML and Body

```css
html,
body {
    margin: 0;
    padding: 0;
    width: 100%;
}
```

### `html, body`

This selects both the HTML root element and the body element.

### `margin: 0`

Removes the browser's default outer margin.

Browsers commonly apply an 8px default margin to the body. Removing it prevents unwanted spacing around the website.

### `padding: 0`

Removes the default inner spacing.

### `width: 100%`

Makes the HTML and body occupy the full available width.

---

# 3. Navbar

```css
.navbar {
    width: 100%;
    padding: 2vh 5vw;
    font-size: 0;
}
```

### `.navbar`

Selects the element with the class `navbar`.

### `width: 100%`

Makes the navbar occupy the full available width.

### `padding: 2vh 5vw`

The shorthand syntax is:

```css
padding: vertical horizontal;
```

Therefore:

* `2vh` adds vertical padding equal to 2% of the viewport height.
* `5vw` adds horizontal padding equal to 5% of the viewport width.

### `font-size: 0`

Removes whitespace gaps between inline-block elements in the HTML.

This is useful when placing the logo, navigation links, and username side by side using `inline-block`.

---

# 4. Navbar Child Elements

```css
.logo,
.nav-links,
.username {
    display: inline-block;
    vertical-align: middle;
    font-size: 16px;
}
```

### `.logo, .nav-links, .username`

This is a grouped selector. It applies the same CSS properties to all three classes.

### `display: inline-block`

Places elements beside each other while allowing them to have specified widths and heights.

Unlike `display: inline`, inline-block elements can have width, height, padding, and margins.

### `vertical-align: middle`

Aligns the inline-block elements vertically relative to the line they occupy.

### `font-size: 16px`

Restores the text size because the parent navbar has `font-size: 0`.

---

# 5. Logo

```css
.logo {
    width: 25%;
    font-size: 2vw;
    font-weight: bold;
    color: #37474f;
}
```

### `width: 25%`

Allocates 25% of the navbar's content width to the logo.

### `font-size: 2vw`

Sets the font size to 2% of the viewport width.

The font becomes smaller on narrow screens and larger on wider screens.

### `font-weight: bold`

Makes the logo text bold.

### `color: #37474f`

Applies a dark blue-gray text color.

---

# 6. Navigation Links

```css
.nav-links {
    width: 50%;
    text-align: center;
}
```

### `width: 50%`

Allocates 50% of the navbar's content width to the navigation links.

### `text-align: center`

Centers the navigation links within their allocated area.

## Individual Navigation Links

```css
.nav-links a {
    display: inline;
    margin: 0 1vw;
    color: #37474f;
    text-decoration: none;
}
```

### `.nav-links a`

Selects every anchor element inside the `.nav-links` container.

### `display: inline`

Keeps the navigation links on the same line.

### `margin: 0 1vw`

Adds:

* 0 vertical margin.
* 1vw horizontal margin.

This creates spacing between the links.

### `color: #37474f`

Sets the navigation link text color.

### `text-decoration: none`

Removes the default underline from the links.

---

# 7. Username

```css
.username {
    width: 25%;
    padding: 1vh 1vw;
    background-color: #e1f5fe;
    border-radius: 8px;
    text-align: center;
}
```

### `width: 25%`

Allocates 25% of the navbar's content width to the username area.

If the username background is too wide, use:

```css
width: auto;
```

This allows the background to fit the content and padding.

### `padding: 1vh 1vw`

Adds vertical and horizontal inner spacing.

### `background-color: #e1f5fe`

Sets a light blue background.

### `border-radius: 8px`

Rounds the corners of the username box.

### `text-align: center`

Centers the username text.

---

# 8. Hero Section

```css
.hero-section {
    width: 90vw;
    height: 80vh;
    margin: 5vh 5vw;
    font-size: 0;
}
```

### `width: 90vw`

Sets the hero section width to 90% of the viewport width.

### `height: 80vh`

Sets the hero section height to 80% of the viewport height.

### `margin: 5vh 5vw`

Adds:

* 5vh vertical margin.
* 5vw horizontal margin.

### `font-size: 0`

Removes whitespace gaps between inline-block hero columns.

---

# 9. Hero Columns

```css
.hero-left,
.hero-right {
    display: inline-block;
    vertical-align: middle;
    width: 50%;
    height: 100%;
    font-size: 16px;
}
```

### `display: inline-block`

Places the left and right hero divs side by side.

### `vertical-align: middle`

Aligns the columns vertically.

### `width: 50%`

Each column occupies half of the hero section's width.

### `height: 100%`

Each column occupies the full height of the hero section.

### `font-size: 16px`

Restores normal text size inside the hero columns.

---

# 10. Left Hero Div

```css
.hero-left {
    padding: 10vh 3vw;
}
```

### `padding: 10vh 3vw`

Adds:

* 10vh vertical padding.
* 3vw horizontal padding.

This creates space between the heading, paragraph, button, and the edges of the left div.

---

# 11. Hero Heading

```css
.hero-left h1 {
    font-size: 3vw;
    color: #455a64;
    margin: 0 0 2vh;
}
```

### `.hero-left h1`

Selects the `h1` heading inside the left hero div.

### `font-size: 3vw`

Makes the heading responsive to the viewport width.

### `color: #455a64`

Sets the heading to a blue-gray color.

### `margin: 0 0 2vh`

Sets:

* Top margin: 0.
* Right margin: 0.
* Bottom margin: 2vh.
* Left margin: 0.

This adds space below the heading.

## Highlighted Heading Text

```css
.hero-left h1 span {
    color: #03a9f4;
}
```

Selects the `span` inside the heading.

### `color: #03a9f4`

Changes the highlighted text to light blue.

---

# 12. Paragraph

```css
.hero-left p {
    font-size: 1.2vw;
    line-height: 1.6;
    color: #78909c;
}
```

### `font-size: 1.2vw`

Sets the paragraph font size to 1.2% of the viewport width.

### `line-height: 1.6`

Sets the line spacing to 1.6 times the font size.

This improves readability.

### `color: #78909c`

Sets a lighter blue-gray paragraph color.

---

# 13. Booking Button

```css
.book-button {
    width: 15vw;
    height: 5vh;
    padding: 0;
    border: none;
    border-radius: 8px;
}
```

### `width: 15vw`

Sets the button width to 15% of the viewport width.

### `height: 5vh`

Sets the button height to 5% of the viewport height.

### `padding: 0`

Removes inner padding so it does not add unexpected height.

### `border: none`

Removes the default button border.

### `border-radius: 8px`

Rounds the button corners.

## Button Gradient

```css
background: linear-gradient(
    to right,
    #03a9f4,
    #0288d1
);
```

### `background`

Sets the background of the button.

### `linear-gradient`

Creates a smooth transition between colors.

### `to right`

The gradient starts on the left and moves toward the right.

### `#03a9f4`

Light blue on the left.

### `#0288d1`

Darker blue on the right.

## Button Text and Cursor

```css
color: white;
font-size: 1vw;
cursor: pointer;
```

### `color: white`

Makes the button text white.

### `font-size: 1vw`

Makes the button text responsive.

### `cursor: pointer`

Changes the mouse cursor to a hand when hovering over the button.

---

# 14. Right Hero Image

```css
.hero-right img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    display: block;
}
```

### `width: 100%`

Makes the image fill the width of its parent div.

### `height: 100%`

Makes the image fill the available height.

### `object-fit: contain`

Keeps the entire image visible while maintaining its original aspect ratio.

Empty space may appear if the image and container have different proportions.

### `display: block`

Removes the default inline image gap below the image.

## Alternative: Cover

```css
object-fit: cover;
```

This makes the image cover the entire area, but some parts of the image may be cropped.

---

# 15. Tablet Media Query

```css
@media (max-width: 768px) {
```

This media query applies when the viewport width is 768px or less.

It is useful for tablets and smaller screens.

## Tablet Logo

```css
.logo {
    width: 30%;
    font-size: 3vw;
}
```

### `width: 30%`

Allocates 30% width to the logo.

### `font-size: 3vw`

Adjusts the logo font size for smaller screens.

## Tablet Navigation

```css
.nav-links {
    width: 45%;
}
```

Allocates 45% width to the navigation links.

```css
.nav-links a {
    margin: 0 0.5vw;
    font-size: 2vw;
}
```

Reduces the spacing between links and adjusts their font size.

## Tablet Username

```css
.username {
    width: 25%;
    font-size: 2vw;
}
```

Keeps the username area at 25% width and makes its text responsive.

## Tablet Hero Height

```css
.hero-section {
    height: auto;
}
```

Allows the hero section height to be determined by its content instead of remaining fixed at 80vh.

## Tablet Hero Columns

```css
.hero-left,
.hero-right {
    width: 100%;
    height: auto;
}
```

Each hero column occupies the full available width.

The columns stack vertically.

## Tablet Left Padding

```css
.hero-left {
    padding: 5vh 5vw;
}
```

Reduces the vertical padding on smaller screens.

## Tablet Heading

```css
.hero-left h1 {
    font-size: 6vw;
}
```

Increases the heading size for tablet readability.

## Tablet Paragraph

```css
.hero-left p {
    font-size: 3vw;
}
```

Increases paragraph text size for readability.

## Tablet Button

```css
.book-button {
    width: 35vw;
    height: 7vh;
    font-size: 2.5vw;
}
```

### `width: 35vw`

Makes the button wider on a tablet.

### `height: 7vh`

Makes the button taller.

### `font-size: 2.5vw`

Adjusts the button text size.

## Tablet Image Area

```css
.hero-right {
    height: 45vh;
}
```

Sets the image area height to 45% of the viewport height.

---

# 16. Mobile Media Query

```css
@media (max-width: 480px) {
```

This media query applies when the viewport width is 480px or less.

It is useful for smartphones.

## Mobile Navbar

```css
.navbar {
    padding: 2vh 3vw;
}
```

Reduces the navbar's horizontal padding on narrow screens.

## Mobile Logo

```css
.logo {
    width: 100%;
    text-align: center;
    font-size: 6vw;
    margin-bottom: 2vh;
}
```

### `width: 100%`

Makes the logo occupy a full row.

### `text-align: center`

Centers the logo.

### `font-size: 6vw`

Enlarges the logo text for mobile.

### `margin-bottom: 2vh`

Adds space below the logo.

## Mobile Navigation Links

```css
.nav-links {
    width: 75%;
    text-align: left;
}
```

The navigation links occupy 75% of the row and are aligned to the left.

```css
.nav-links a {
    font-size: 3vw;
    margin: 0 1vw;
}
```

Adjusts the link font size and spacing.

## Mobile Username

```css
.username {
    width: 25%;
    font-size: 3vw;
    padding: 1vh 0;
}
```

### `width: 25%`

Allocates 25% width to the username area.

### `font-size: 3vw`

Makes the username text responsive.

### `padding: 1vh 0`

Adds vertical padding and removes horizontal padding.

## Mobile Hero Section

```css
.hero-section {
    width: 94vw;
    margin: 3vh 3vw;
}
```

### `width: 94vw`

Makes the hero section occupy 94% of the viewport width.

### `margin: 3vh 3vw`

Adds smaller spacing around the hero section.

## Mobile Heading

```css
.hero-left h1 {
    font-size: 8vw;
}
```

Makes the heading larger on mobile.

## Mobile Paragraph

```css
.hero-left p {
    font-size: 4vw;
}
```

Increases paragraph text size for mobile readability.

## Mobile Button

```css
.book-button {
    width: 50vw;
    height: 7vh;
    font-size: 3.5vw;
}
```

### `width: 50vw`

Makes the button wider on mobile.

### `height: 7vh`

Makes the button taller.

### `font-size: 3.5vw`

Adjusts the button text size.

## Mobile Image Area

```css
.hero-right {
    height: 35vh;
}
```

Sets the image area height to 35% of the viewport height.

---

# 17. Important CSS Concepts

## Viewport Width — vw

`1vw` equals 1% of the viewport width.

Example:

```css
div {
    width: 50vw;
}
```

The div occupies 50% of the viewport width.

## Viewport Height — vh

`1vh` equals 1% of the viewport height.

Example:

```css
div {
    height: 80vh;
}
```

The div occupies 80% of the viewport height.

## Percentage Width

```css
div {
    width: 50%;
}
```

The width is calculated relative to the containing block.

## Margin

Margin creates space outside an element.

```css
margin: 10vh 25vw;
```

This adds vertical and horizontal outside spacing.

## Padding

Padding creates space inside an element.

```css
padding: 2vh 5vw;
```

This adds inner spacing around the content.

## Border

A border surrounds an element.

```css
border: 4px solid black;
```

This creates a 4px solid black border.

## Display: Inline

```css
display: inline;
```

Elements remain in the same line and generally do not accept width and height in the same way as block or inline-block elements.

## Display: Inline-Block

```css
display: inline-block;
```

Elements remain beside each other while accepting width, height, padding, and margins.

## Media Query

```css
@media (max-width: 768px) {
    /* CSS rules */
}
```

Applies CSS rules when the viewport width is 768px or less.

---

# 18. Important Note About the Assignment

The CSS uses inline-block, viewport units, and media queries to make the website responsive.

However, a stacked mobile hero section may become taller than the viewport. Therefore, it may require scrolling on smaller screens.

If the assignment requires the entire page to fit on every screen without scrolling, the layout needs additional height and spacing adjustments.

Also, if you require exactly 25% left and right spacing and 10% top and bottom spacing for the hero section, remember that the navbar's height must be considered separately.

---

# Summary

The main CSS concepts used in this project are:

1. Universal selector (`*`)
2. Box sizing (`border-box`)
3. Viewport units (`vw`, `vh`)
4. Inline-block layout
5. Margins and padding
6. Background gradients
7. Responsive images
8. Media queries
9. Responsive typography
10. Navbar and hero section layout

These properties work together to create a responsive laundry services website without using Flexbox or absolute/relative positioning.
