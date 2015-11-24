# SASS NAMED COLORS

A Sass micro-library featuring a standardized list of 1,500+ named colors. No need to puzzle out hex values; just use `k-color(emerald)`, `k-color(monsoon)`, `k-color(cloud)`, and so on. Also features aliased functions and variable names for those who prefer to work with colo**u**rs ;)

Original list of colors compiled by [Chirag Mehta](http://chir.ag/projects/name-that-color/) and converted to Sass by [James Pearson](https://github.com/FearMediocrity/sass-color-palettes). Additional credit is due to Erskine Design for the article [Friendlier colour names with Sass maps](http://erskinedesign.com/blog/friendlier-colour-names-sass-maps/). This project expands on their work by providing a bit of syntactic sugar as well as npm and Bower packages.

[Read the announcement post on my blog](http://synapticism.com/dev/a-sass-micro-library-for-working-with-named-colours/).



## Installation

Download/clone this repo or install with npm (`npm install sass-named-colors --save-dev`) or Bower (`bower install sass-named-colors -D`). Import into your project with `@import "sass-named-colors/named-colors"`.

This library has no dependencies. Requirements: Sass 3.3+.



## Usage

This library ships with one function: `k-color($color, $fallback, $library)`. Only `$color` is required; the remaining arguments are mainly for internal use. Example:

```scss
.element {
  color: k-color(red);
  &:hover {
    color: rgba(k-color(orange), .9);
  }
}
```

To extend the built-in colors on a per-project basis:

```scss
$k-colors: map-merge($k-colors, (
  norse-blue:     #5cb6cc,
  suomi-blue:     #559dd1,
  steel-sky:      #444547,
  jove:           #24221E
));
```

Need a tool to browse the options? Try the color picker on the original [project page](http://chir.ag/projects/name-that-color/).



## Spelling

You can also use international spelling with all relevant functions and variables and swap "color" for "colour". Whatever you do, be consistent in what you use; don't add custom colors to `$k-colors` and then attempt to call them with `k-colours()` as this function will be checking `$k-colours`. Don't want alternate spelling? Ignore it and you won't be affected at all.



## License

MIT/GPLv3.
