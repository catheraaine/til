## Storing Colors in Variables with Sass

[Sass](http://sass-lang.com/), or Syntactically Awesome Style Sheets, is a preprocessor for CSS. You probably know this. I am still learning. Anyway, Sass lets you create variables!

 Using hex value colors over and over can get a bit messy, especially in huge CSS files. It therefore makes sense to store these hex value colors in a variable using Sass.

Variables in Sass are declared at the top of the page, much like regular CSS syntax, but beginning with a `$`:

 ``` sass
$teal: #2FB8AC;
$darkish-blue: #046D8B;
 ```

Then, in the rest of the Sass file, that variable can be used in place of the hex code:

``` sass
body {
  color: $darkish-blue;
  background-color: $teal;
}

```

All kinds of things can be stored in Sass variables, including padding, margin, font stacks, etc. 
