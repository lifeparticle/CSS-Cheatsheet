# Introduction

TODO


# CSS basics

```css

h1 {
  color: blue;
}
```

```
h1: Selector           | Rule/Ruleset
color: Property        |     | Declaration 
red: Property value    |     |
```

## Selectors

| Name                     | Example                      | Code Example                    |
|--------------------------|------------------------------|---------------------------------|
| Universal Selector       | `*`                          | `* { margin: 0; }`                    |
| Type Selector            | `div`                        | `div { color: blue; }`                |
| Class Selector           | `.class-name`                | `.class-name { font-size: 14px; }`    |
| ID Selector              | `#id-name`                   | `#id-name { background: yellow; }`    |
| Attribute Selector       | `[type="text"]`              | `[type="text"] { border: 1px solid; }`|
| Descendant Selector      | `div p`                      | `div p { margin: 10px; }`             |
| Child Selector           | `div > p`                    | `div > p { padding: 5px; }`           |
| Adjacent Sibling Selector| `h1 + p`                     | `h1 + p { color: green; }`            |
| General Sibling Selector | `h1 ~ p`                     | `h1 ~ p { font-style: italic; }`      |
| Grouping Selector        | `h1, h2, h3`                 | `h1, h2, h3 { margin-bottom: 10px; }`|
| Pseudo-class Selector    | `a:hover`                    | `a:hover { text-decoration: underline; }`|
| Pseudo-element Selector  | `p::before`                  | `p::before { content: "Note: "; }`|
| Attribute Presence       | `[title]`                    | `[title] { color: red; }`       |
| Attribute Value          | `[title="value"]`            | `[title="value"] { font-weight: bold; }`|
| Attribute Starts With    | `[title^="value"]`           | `[title^="value"] { color: blue; }`|
| Attribute Ends With      | `[title$="value"]`           | `[title$="value"] { color: green; }`|
| Attribute Contains       | `[title*="value"]`           | `[title*="value"] { color: orange; }`|
| Negation Selector        | `:not(selector)`             | `:not(p) { color: gray; }`      |
| First Child              | `:first-child`               | `div:first-child { font-size: 18px; }`|
| Last Child               | `:last-child`                | `div:last-child { font-size: 12px; }`|
| nth Child                | `:nth-child(2)`              | `div:nth-child(2) { color: purple; }`|
| nth Last Child           | `:nth-last-child(2)`         | `div:nth-last-child(2) { color: pink; }`|
| Only Child               | `:only-child`                | `div:only-child { color: brown; }`|
| First of Type            | `:first-of-type`             | `p:first-of-type { margin-top: 20px; }`|
| Last of Type             | `:last-of-type`              | `p:last-of-type { margin-bottom: 20px; }`|
| nth of Type              | `:nth-of-type(2)`            | `p:nth-of-type(2) { color: teal; }`|
| nth Last of Type         | `:nth-last-of-type(2)`       | `p:nth-last-of-type(2) { color: navy; }`|
| Only of Type             | `:only-of-type`              | `p:only-of-type { color: maroon; }`|
| Empty                    | `:empty`                     | `div:empty { display: none; }`  |
| Enabled                  | `:enabled`                   | `input:enabled { background: white; }`|
| Disabled                 | `:disabled`                  | `input:disabled { background: gray; }`|
| Checked                  | `:checked`                   | `input:checked { border: 2px solid blue; }`|
| Before                   | `::before`                   | `p::before { content: "Start: "; }`|
| After                    | `::after`                    | `p::after { content: " End."; }` |
| Placeholder              | `::placeholder`              | `input::placeholder { color: gray; }`|



```html
<div>
    <p>1. This paragraph will be selected.</p>
</div>
<div>
    <p>2. This paragraph will not be selected</p>
    <p>3. This paragraph will not be selected</p>
</div>
```

```css
p:only-of-type {
  color: red;
}
```

<img width="298" alt="Screen Shot 2024-06-08 at 3 05 51 pm" src="https://github.com/lifeparticle/CSS-Cheatsheet/assets/1612112/94715b23-cced-410b-bf2a-e2839cbd2b3c">


## Box model

<img width="295" alt="Screen Shot 2024-06-06 at 10 03 31 pm" src="https://github.com/lifeparticle/CSS-Cheatsheet/assets/1612112/0dcb25bd-8c05-4e4a-9f47-e43d864436f3">

## Pseudo-classes

| Pseudo-class       | Description                                                                   |
|--------------------|-------------------------------------------------------------------------------|
| `:hover`           | Applies styles when the user hovers over an element.                          |
| `:active`          | Applies styles when an element is activated (e.g., when a user clicks on it). |
| `:focus`           | Applies styles when an element has focus.                                     |
| `:visited`         | Applies styles to visited links.                                              |
| `:link`            | Applies styles to unvisited links.                                            |
| `:first-child`     | Applies styles to the first child of an element.                              |
| `:last-child`      | Applies styles to the last child of an element.                               |
| `:nth-child(n)`    | Applies styles to the nth child of an element.                                |
| `:nth-of-type(n)`  | Applies styles to the nth child of a specified type of its parent.            |
| `:first-of-type`   | Applies styles to the first child of a specified type of its parent.          |
| `:last-of-type`    | Applies styles to the last child of a specified type of its parent.           |
| `:only-child`      | Applies styles to an element that is the only child of its parent.            |
| `:only-of-type`    | Applies styles to an element that is the only child of its type of its parent.|
| `:not(selector)`   | Applies styles to elements that do not match the selector.                    |
| `:empty`           | Applies styles to elements that have no children.                             |
| `:checked`         | Applies styles to checked form elements (e.g., radio buttons, checkboxes).    |
| `:disabled`        | Applies styles to disabled form elements.                                     |
| `:enabled`         | Applies styles to enabled form elements.                                      |
| `:target`          | Applies styles to an element that is the target of the current URL fragment.  |
| `:root`            | Applies styles to the document's root element.                                |

## Pseudo-elements

| Pseudo-element     | Description                                                        |
|--------------------|--------------------------------------------------------------------|
| `::before`         | Inserts content before an element's content.                       |
| `::after`          | Inserts content after an element's content.                        |
| `::first-letter`   | Applies styles to the first letter of an element.                  |
| `::first-line`     | Applies styles to the first line of an element.                    |
| `::selection`      | Applies styles to the portion of an element that is selected.      |
| `::placeholder`    | Applies styles to the placeholder text of an input element.        |
| `::marker`         | Applies styles to the marker of a list item.                       |
| `::backdrop`       | Applies styles to the backdrop of an element.                      |
| `::cue`            | Applies styles to WebVTT cues.                                     |
| `::spelling-error` | Applies styles to text identified as a spelling error.             |
| `::grammar-error`  | Applies styles to text identified as a grammatical error.          |


## Transition

https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties

```css
div {
  transition-property: margin-right;
  transition-duration: 3s;
  transition-delay: 5s;
}
```

```css
div {
  transition: <property> <duration> <timing-function> <delay>;
}
```

```css
transition-timing-function: ease;
transition-timing-function: ease-in;
transition-timing-function: ease-out;
transition-timing-function: ease-in-out;
transition-timing-function: linear;
transition-timing-function: step-start;
transition-timing-function: step-end;
```

# My CSS Articles

1. [How To Create a User Interface Using CSS Grid](https://medium.com/geekculture/how-to-create-a-user-interface-using-css-grid-738d0b51282)

# Books
1. https://www.refactoringui.com/

# Tools
https://cssstats.com/

# Resources
1. https://css-tricks.com/building-a-scalable-css-architecture-with-bem-and-utility-classes/
2. https://github.com/jareware/css-architecture
3. https://developer.mozilla.org/en-US/docs/Web/CSS/clamp
4. https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity
5. http://smacss.com/
6. https://frontendmasters.com/courses/css-variables/dry-fallback-strategies/
7. https://open-props.style/
8. https://nerdy.dev/
9. https://styleguide.github.com/
10. https://bradfrost.com/blog/post/atomic-web-design/
11. https://css-weekly.com/
12. https://frontendfoc.us/
13. https://www.lightningdesignsystem.com/components/overview/
14. https://www.youtube.com/watch?v=7hYOLLO2gc4&t=1357s&ab_channel=YouGottaLoveFrontend
15. https://courses.rachelnabors.com/p/web-animation-essentials-css-animations-and-transitions
