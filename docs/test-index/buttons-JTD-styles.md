---
title: Button Styles in Just the Docs
parent: Some Jekyll Markdown Guidelines
nav_order: 2
---

Here are the button style sheet copied from JTD.

```css
// Buttons and things that look like buttons
// stylelint-disable color-named

.btn {
  display: inline-block;
  box-sizing: border-box;
  padding: 0.3em 1em;
  margin: 0;
  font-family: inherit;
  font-size: inherit;
  font-weight: 500;
  line-height: 1.5;
  color: $link-color;
  text-decoration: none;
  vertical-align: baseline;
  cursor: pointer;
  background-color: $base-button-color;
  border-width: 0;
  border-radius: $border-radius;
  box-shadow:
    0 1px 2px rgba(0, 0, 0, 0.12),
    0 3px 10px rgba(0, 0, 0, 0.08);
  appearance: none;

  &:focus {
    text-decoration: none;
    outline: none;
    box-shadow: 0 0 0 3px rgba(blue, 0.25);
  }

  &:focus:hover,
  &.selected:focus {
    box-shadow: 0 0 0 3px rgba(blue, 0.25);
  }

  &:hover,
  &.zeroclipboard-is-hover {
    color: darken($link-color, 2%);
  }

  &:hover,
  &:active,
  &.zeroclipboard-is-hover,
  &.zeroclipboard-is-active {
    text-decoration: none;
    background-color: darken($base-button-color, 1%);
  }

  &:active,
  &.selected,
  &.zeroclipboard-is-active {
    background-color: darken($base-button-color, 3%);
    background-image: none;
    box-shadow: inset 0 2px 4px rgba(0, 0, 0, 0.15);
  }

  &.selected:hover {
    background-color: darken(#dcdcdc, 5%);
  }

  &:disabled,
  &.disabled {
    &,
    &:hover {
      color: rgba(102, 102, 102, 0.5);
      cursor: default;
      background-color: rgba(229, 229, 229, 0.5);
      background-image: none;
      box-shadow: none;
    }
  }
}

.btn-outline {
  color: $link-color;
  background: transparent;
  box-shadow: inset 0 0 0 2px $grey-lt-300;

  &:hover,
  &:active,
  &.zeroclipboard-is-hover,
  &.zeroclipboard-is-active {
    color: darken($link-color, 4%);
    text-decoration: none;
    background-color: transparent;
    box-shadow: inset 0 0 0 3px $grey-lt-300;
  }

  &:focus {
    text-decoration: none;
    outline: none;
    box-shadow:
      inset 0 0 0 2px $grey-dk-100,
      0 0 0 3px rgba(blue, 0.25);
  }

  &:focus:hover,
  &.selected:focus {
    box-shadow: inset 0 0 0 2px $grey-dk-100;
  }
}

.btn-primary {
  @include btn-color($white, $btn-primary-color);
}

.btn-purple {
  @include btn-color($white, $purple-100);
}

.btn-blue {
  @include btn-color($white, $blue-000);
}

.btn-green {
  @include btn-color($white, $green-100);
}

.btn-reset {
  background: none;
  border: none;
  margin: 0;
  text-align: inherit;
  font: inherit;
  border-radius: 0;
  appearance: none;
}
```
