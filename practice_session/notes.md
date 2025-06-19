## This is notes for only HTML and CSS where im just revisiting the concepts.

### Sizes

em : directly relative to the parent

```html
<div style="{font-size" : 20px}>
  <h1 style="{font-size" : 2em}>Child</h1>
  <-- Then the actual size of h1 will be 20*2 => 40px ->
</div>
```

But, rem is opposite

rem : it is relative to HTML.

## Box Model

If you want to shift the boxes or content of div you can use the formula :

width: 200 + padding: 20*2 + border: 10*2 = 260px so you can use margin-left to push the box 260px.

Just remember the formula.

## Specificity

id
attribute li[draggable]
class
element

```css
p {
  color: red !important;
}
```

## combining selectors

.glass > img ==> It will check img in glass class.
.red a => in class red all the styles will be applied to a
h1,h2 => all the styles should be applioed to all h1 and h2.
h1.done#red => more specific but remember to put tag first
seke slec.class => in seke the slec in that class.

### Display

- Inline => U cnt change the height and width of this display because it takes the space of the content only.
- Inline-block => U can set height and width.
- None => Disappear

```css
/* THis will move image to left and the all the other content will float around it.*/
img {
  float: left;
}

/* There is clear if you dont want to float around the img or some content : left,right,both*/

footer {
  clear: left;
}
```

### Position

```css

/* Static => Defualt */

div{
    position: static;
    left: 50px
    top: 50px
}

/* Reltive */
/* relative to the default position */


div {
    postion: relative;
    left: 50px;
    right: 50px;
}

/* So it will move from its default positon to 50px left and right. */

/* Absolute */
/* Position relative to nearest positioned ancestor or top left corner of webpage */
/* If parent div is positioned to relative so the inner box with absolute will be relaive to its nearest parent box. */

div {
    position: absolute;
    left: 50px;
    right: 50px;
}

/* fixed */
/* Position relative to top left corner of browser window */


div {
    position: fixed;
    left: 50px;
    right: 50px;
}

```

## Responsive Websites

- Media Query
  @media (max-width: 600px) {
  Css for screens below or equal to 600px wide
  }

@media (min-width: 600px) and (max-width: 900px) {
Styles for screens between 600px and 900px
}

@media (max-width: 600px) and (min-width: 900px) {
Styles for screens less than 600px and greater than 900px
}

## Width

<!-- Specificity -->

content width < Width < Flex-basis < min/max-width

---

## Grid

grid-tempelate-columns
grid-tempelate-rows
grid-tempelate : for both rows / columns

// Remember: if you set grid-templeate-rows: 100px auto then the auto will be fit content, But for columns auto will be 100% of screen size available

// we can use minmax(400px, 800px) stop at 400px and grow it 800px;

// If in future you have many components then you can use grid-auto-columns/rows

// Items: grid column shorthand for grid-column-start and end.

## Design

### Color theory

- Red : Love, Engertic
- Green : Freshness, Safety, Growth
- Yellow : Joy, Intellect, Attention
- Blue : Stability, Trust, Setenity
- Purple : Royalty, Wealth, Feminity

### Typography

- serif => pushed down (Historic)
  - Traditional, Stable, Respectable
- Sans-serif
  - Sensible, Simple, Straightfoward
- Script
  - Personal Creative Elegant
- Display
  - Friendly, Loud, Amusing
- Modern
  - Stylish, Chic, Smart

### UI Design

Try to keep only 40-60 char per line that feel comfortable to read.

- Alignment matters (use less alignment points)
- Whitespace
- Audience (design for them)
- Layout

### UX Design

- Simplicity
- Consistency
- Use F-Layout & Z-layout
- All Platform Design
