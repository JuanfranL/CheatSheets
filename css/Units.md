
# CSS Units Guide

This guide summarizes the differences between CSS units, their usage, and practical examples.

## Types of Units

### Absolute Units
- **`px` (pixels)**: The only absolute unit that does not change. Best for fixed-size elements.

### Relative Units
Relative units depend on other variables, such as:
- **`rem`** and **`em`**: Relative to the root font size or parent element.
- **`%`**: Relative to the parent container size.
- **`vw`** and **`vh`**: Relative to the viewport's width and height.
- **`vmin`** and **`vmax`**: Relative to the minimum or maximum size of the viewport.
- **`fr`**: Fraction of the available space in a grid container.
- **`ch`**: Width of the "0" character of the font.

## Unit Comparison Table

| Unit       | Relative To                     | Primary Use                     |
|------------|---------------------------------|----------------------------------|
| `px`       | None (absolute)                 | Fixed sizes                     |
| `rem`      | Root font size                  | Scalable text                   |
| `em`       | Parent element font size        | Relative scaling                |
| `%`        | Parent container                | Flexible layouts                |
| `vw`       | Viewport width                  | Responsive designs              |
| `vh`       | Viewport height                 | Responsive heights              |
| `vmin`     | Smaller dimension of viewport   | Responsive designs              |
| `vmax`     | Larger dimension of viewport    | Responsive designs              |
| `fr`       | Grid container                  | Grid layouts                    |
| `ch`       | Width of "0" character          | Predictable text widths         |

## Practical Examples

### Using `rem` for Scalable Text
```css
html {
    font-size: 16px;
}

h1 {
    font-size: 2rem; /* 32px */
}

p {
    font-size: 1rem; /* 16px */
}
```

### Responsive Design with `vw` and `vh`
```css
.hero {
    height: 100vh; /* Full viewport height */
    font-size: 5vw; /* Scales with viewport width */
}
```

### Flexible Layouts with `%`
```css
.container {
    width: 80%; /* Occupies 80% of the parent container */
    padding: 10px;
}
```

### Combining Units with `clamp()`
```css
h1 {
    font-size: clamp(18px, 5vw, 36px); /* Scales between 18px and 36px */
}
```

### Grid Layout with `fr`
```css
.grid {
    display: grid;
    grid-template-columns: 1fr 2fr; /* First column 1 fraction, second column 2 fractions */
}
```

## Conclusion
Understanding when to use each unit depends on your goals. For fixed dimensions, use absolute units like `px`. For responsive and scalable designs, leverage relative units such as `rem`, `vw`, and `fr`. Mix and match units for the most adaptable results!