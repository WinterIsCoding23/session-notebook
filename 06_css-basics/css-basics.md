## CSS syntax

The structure of how to write CSS is also called **ruleset**. It consists of four parts:

![CSS syntax](assets/css-syntax.png)

| Part           | Description                                                                                       |
| -------------- | ------------------------------------------------------------------------------------------------- |
| Selector       | Addresses the element(s) to style                                                                 |
| Declaration    | Defines what to change and contains pairs of `property` and `property value`                      |
| Property       | The name of the property to change                                                                |
| Property Value | The value assigned to the property, e.g for the property `color` we use the property value `blue` |

A ruleset can have `multiple declarations`:

```css
h1 {
  color: blue;
  font-size: 3rem;
  text-align: center;
}
```

You could also select multiple elements and style them with the same ruleset:

```css
h1,
h2,
h3 {
  color: red;
}
```

---

## Basic Selectors

There are different CSS selectors you can use to style elements. The most common ones are:

- **Universal selector** `*` selects all elements.
- **Element or Type selector**, like `article`, selects all elements of a specific type.
  ```css
  article {
    color: red;
  }
  ```
- **Class selector**, like `.class-name`, selects all elements with the specified class.
  ```css
  .my-cool-class {
    color: hotpink;
  }
  ```
  ```html
  <aside class="my-cool-class">...</aside>
  ```

> ❗️ In theory you could also use element IDs as selectors, but this is bad practice and must be
> avoided.

---

## CSS Properties

There are a lot of CSS properties and you will discover new ones every day. Therefore the following
list shows only a few examples:

| Property           | Effect                                         |
| ------------------ | ---------------------------------------------- |
| `color`            | Color of an element´s text                     |
| `font-size`        | Defines the size of a font                     |
| `text-align`       | Defines the alignment of text                  |
| `background-color` | Background color of an element                 |
| `border`           | Defines the border of an element.              |
| `padding`          | Defines the padding of an element.             |
| `margin`           | Defines the margin of an element.              |
| `width`            | This property defines the width of an element. |

> 💡 You can find more properties in the
> [CSS Properties Reference](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference#index) on
> MDN.

## Box Model

All elements of a website are wrapped in a **box model**. It's a way to define the size and position
of an element. There are four different parts: `content`, `padding`, `border` and `margin`.

| box model part | Function                                                 |
| -------------- | -------------------------------------------------------- |
| `content`      | The actual content of the element.                       |
| `padding`      | Space between the content and the border of the element. |
| `border`       | The border of the element.                               |
| `margin`       | The space around the border and other elements.          |

The property `box-sizing` changes the way how the `width` and `height` of an element is calculated.
The default value is `content-box`. The values of `width` and `height` set the size of the "content
box". With the value `border-box`, the size of the "border box" is set instead.

```css
* {
  box-sizing: border-box;
}
```

Now, the `width` property defines the size of the border box, padding and border width are
subtracted to calculate the available space for the content.

<img src="./assets/box-model.png" width="500" alt="Box model">
