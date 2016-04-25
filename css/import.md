## Sass: The Import(ant) Rule

"Partials" are small pieces of code that combine to make finished documents.

In Sass, partials keep code organized by separating styles into separate `.scss` files and combining them at compile time (Sass is a preprocessor, meaning the code must be compiled into functional CSS before it can be used on the web).

To `import` partials into a single Sass file, we use the `@import` rule.

A Sass file does not need an extension (or prefixed underscore, see note below) to be recognized by the compiler. Say we have a file called `_reset.scss` in our `CSS` directory. That file would be imported like this:

``` sass
@import "CSS/reset";
```

You can import many partials into your main `.scss` file, creating a complete Sass document.

*Note: It is a good idea to name partials with a leading underscore (such as `_reset.scss`), so the compiler knows not to create a separate css file for each.*
