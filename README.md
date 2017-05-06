# Entity

A ([revamped](https://github.com/jeremy-green/entity)) Sass function that will output properly encoded entities.

## Why :thinking:

No clue. I came across https://dev.w3.org/html5/html-author/charref and thought
it would be fun. I ran a Node script that output the file then wrote some tests.

## Usage

The `entity` function accepts the actual character, the HTML name without the
ampersand and semi-colon or the decimal number.

```scss
body {
  &:after {
    content: entity('€');
  }
}
```

or

```scss
body {
  &:after {
    content: entity('euro');
  }
}
```

will output

```css
body:after {
  content: "\20AC";
}
```
