# Bootstrap(V5)

Some elements to modify the properties

### **Containers**

Bootstrap 5 also requires a containing element to wrap site contents.

There are two container classes to choose from:

1. The `.container` class provides a responsive **fixed width container**
2. The `.container-fluid` class provides a **full width container**, spanning the entire width of the viewport
    
    ![Untitled](Bootstrap(V5)%20cb0d8940735e4c0bba66464bf4ed009f/Untitled.png)
    

To summarize:

- **`.container`** creates a fixed-width container with responsive behavior.
- **`.container-fluid`** creates a full-width container that spans the entire viewport.

You can choose between these classes based on your specific layout requirements and how you want the content to be displayed within the container.

### Container Padding and Margin

By default, containers have left and right padding, with no top or bottom padding. Therefore, we often use **spacing utilities**, such as extra padding and margins to make them look even better. For example, `.pt-5` means "add a large **top padding**":

```html
<div class="container pt-5"></div>
```

### **Container Border and Color**

First output color: none(default white)

Second output color: Blue

Third output color: Black

```html
<div class="container p-5 my-5 border"></div>

<div class="container p-5 my-5 bg-dark text-white"></div>

<div class="container p-5 my-5 bg-primary text-white"></div>
```

**For text color ”text-primary”**

he classes for text colors are: `.text-muted`, `.text-primary`, `.text-success`, `.text-info`, `.text-warning`, `.text-danger`, `.text-secondary`, `.text-white`, `.text-dark`, `.text-body` (default body color/often black) and `.text-light`:

### ****Margin and padding****

- `m` - for classes that set `margin`
- `p` - for classes that set `padding`

Where *sides* is one of:

- `t` - for classes that set `margin-top` or `padding-top`
- `b` - for classes that set `margin-bottom` or `padding-bottom`
- `s` - (start) for classes that set `margin-left` or `padding-left` in LTR, `margin-right` or `padding-right` in RTL
- `e` - (end) for classes that set `margin-right` or `padding-right` in LTR, `margin-left` or `padding-left` in RTL
- `x` - for classes that set both `-left` and `-right`
- `y` - for classes that set both `-top` and `-bottom`
- blank - for classes that set a `margin` or `padding` on all 4 sides of the element

Where *size* is one of:

- `0` - for classes that eliminate the `margin` or `padding` by setting it to `0`
- `1` - (by default) for classes that set the `margin` or `padding` to `$spacer * .25`
- `2` - (by default) for classes that set the `margin` or `padding` to `$spacer * .5`
- `3` - (by default) for classes that set the `margin` or `padding` to `$spacer`
- `4` - (by default) for classes that set the `margin` or `padding` to `$spacer * 1.5`
- `5` - (by default) for classes that set the `margin` or `padding` to `$spacer * 3`
- `auto` - for classes that set the `margin` to auto

```html
<div class="grid gap-0 row-gap-3">
  <div class="p-2 g-col-6">Grid item 1</div>
  <div class="p-2 g-col-6">Grid item 2</div>
  <div class="p-2 g-col-6">Grid item 3</div>
  <div class="p-2 g-col-6">Grid item 4</div>
</div>
```