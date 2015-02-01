# SASS NAMED COLORS

A Sass micro-library featuring a standardized list of 1,500+ named colors. No need to puzzle out hex values; just use `emerald`, `monsoon`, `cloud`, `carnation`, and so on.

Original list of colors compiled by [Chirag Mehta](http://chir.ag/projects/name-that-color/) and converted to Sass by [James Pearson](https://github.com/FearMediocrity/sass-color-palettes). This project differs mainly in providing a simple function to access the named color map as well as an install path via Bower.

Additional credit is due to Erskine Design for the article [Friendlier colour names with Sass maps](http://erskinedesign.com/blog/friendlier-colour-names-sass-maps/).



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
```

To extend the default colors on a per project basis:

```language-scss
$k-colors: map-merge($k-colors, (
  norse-blue:     #5cb6cc,
  suomi-blue:     #559dd1,
  steel-sky:      #444547,
  jove:           #24221E
));
```

Need a tool to browse the options? Try the color picker on the original [project page](http://chir.ag/projects/name-that-color/).



## License

MIT/GPLv3.
