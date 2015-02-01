# SASS NAMED COLORS

A Sass micro-library featuring 1,500+ named colors.

Original list of colors compiled by [Chirag Mehta](http://chir.ag/projects/name-that-color/) and converted to Sass by [James Pearson](https://github.com/FearMediocrity/sass-color-palettes). This project differs mainly in providing a simple function to access the named color map.



## Installation

Download/clone this repo or install with Bower: `bower install sass-named-colors -D`. This project has no dependencies. Requirements: Sass 3.3+.



## Usage

This library ships with one function:

```scss
k-color($color);
```

This will return the named color in the `$k-colors` table. You could use this in any number of ways:

```scss
.element {
  color: k-color(red);
  &:hover {
    color: rgba(k-color(orange), .9);
  }
}

To extend the default colors on a per project basis:

```language-scss
$k-colors: map-merge($k-colors, (
  norse-blue:     #5cb6cc,
  suomi-blue:     #559dd1,
  steel-sky:      #444547,
  jove:           #24221E
));
```



## License

MIT/GPLv3.
