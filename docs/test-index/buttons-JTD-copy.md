---
title: Buttons in Just the Docs
parent: Some Jekyll Markdown Guidelines
nav_order: 1
---

# Buttons

This is just a copy of `_sass/buttons.scss` in JTD. I didn't copy over the styles, so this file doesn't appear right.

## Basic button styles

### Links that look like buttons

```html
<div class="code-example" markdown="1">
[Link button](https://just-the-docs.com){: .btn }

[Link button](https://just-the-docs.com){: .btn .btn-purple }
[Link button](https://just-the-docs.com){: .btn .btn-blue }
[Link button](https://just-the-docs.com){: .btn .btn-green }

[Link button](https://just-the-docs.com){: .btn .btn-outline }
</div>
```

```markdown
[Link button](https://just-the-docs.com){: .btn }

[Link button](https://just-the-docs.com){: .btn .btn-purple }
[Link button](https://just-the-docs.com){: .btn .btn-blue }
[Link button](https://just-the-docs.com){: .btn .btn-green }

[Link button](https://just-the-docs.com){: .btn .btn-outline }
```

### Button element

GitHub Flavored Markdown does not support the `button` element, so you'll have to use inline HTML for this:

```html
<div class="code-example">
<button type="button" name="button" class="btn">Button element</button>
</div>
```

```html
<button type="button" name="button" class="btn">Button element</button>
```

## Using utilities with buttons

### Button size

Wrap the button in a container that uses the font-size utility classes (`docs/utilities/typography.md`) to scale buttons:

```html
<div class="code-example" markdown="1">
<span class="fs-6">
[Big ass button](https://just-the-docs.com){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](https://just-the-docs.com){: .btn }
</span>
</div>
```

```markdown
<span class="fs-8">
[Link button](https://just-the-docs.com){: .btn }
</span>

<span class="fs-3">
[Tiny ass button](https://just-the-docs.com){: .btn }
</span>
```

### Spacing between buttons

Use the margin utility classes (`docs/utilities/layout.md`) to add spacing between two buttons in the same block.

```html
<div class="code-example" markdown="1">
[Button with space](https://just-the-docs.com){: .btn .btn-purple .mr-2 }
[Button](https://just-the-docs.com){: .btn .btn-blue }

[Button with more space](https://just-the-docs.com){: .btn .btn-green .mr-4 }
[Button](https://just-the-docs.com){: .btn .btn-blue }
</div>
```

```markdown
[Button with space](https://just-the-docs.com){: .btn .btn-purple .mr-2 }
[Button](https://just-the-docs.com){: .btn .btn-blue }

[Button with more space](https://just-the-docs.com){: .btn .btn-green .mr-4 }
[Button](https://just-the-docs.com){: .btn .btn-blue }
```
