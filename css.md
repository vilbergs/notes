# CSS Notes

## Resources

- Javascript Yellow RGB color rgb(243, 223, 73)
- Flexbox game: https://flexboxfroggy.com

## Media queries
- To utilize browsers' dark mode, use prefers-color-scheme media query.

## Images

### Greyscale images missing an alt tag

```css
img:not([alt]) {
  filter: grayscale(100%);
}
```
