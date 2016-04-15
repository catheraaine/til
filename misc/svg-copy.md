## Duplicating Inline SVG Paths with XLink

Sometimes there is reason to have the same, complicated inline `path` in a single `svg`. In order to DRY up (don't repeat yourself) the code a bit, the `svg` tag can hold an `xlink`, and be duplicated via that link.

The `xlink` needs to be included in the `svg` XML, by adding the `xmlns:xlink` attributes.

```html
<svg xmlns="http://www.w3.org/2000/svg"
xmlns:xlink="http://www.w3.org/1999/xlink"
viewBox="0 0 500 500">
```

Give the `path` an ID.

```html
<path id="squiggle"
d="M333.38,263.31c7.56,2.53,12.24,5.65,11.87,
14.3-0.3,7.05-1.66,14.42-9.75,16-6.84,1.3-14.
5-.95-20.1-4.94-2.63-1.88-6.31-5.19-6.08-8.82
,0.36-5.85,6.39-5.72,7.53-1.46a12.68,12.68,0,
0,1-.22,5.43c-1.39,6.51-4.55,15.08-11.74,16.7
8-6.54,1.55-14.2-2.07-19-6.3A26.79,26.79,0,0,
1,277,278.76c-1.42-8.63,3.06-18.44,12.87-18.4
9a1.5,1.5,0,0,0,0-3,16.13,16.13,0,0,0-15.37,1
2c-2.2,7.78.34,16.32,5.11,22.62,8.59,11.33,28
.43,18.3,36.3,2.67,2.63-5.22,6.33-13.86,2.89-
19.55-3-5-9.72-3.2-11.8,1.69-3,6.94,4.25,13.2
1,9.61,16.19,6.45,3.6,15.56,5.6,22.67,2.77,7.
85-3.12,8.92-12.12,9-19.53,0.17-9.29-6-13-14.
12-15.74-1.84-.61-2.62,2.28-0.8,2.89h0Z" />
```

(See all those anchor points? We do not want that mucking up the code!)

Then, with a `use` tag, the same `path` can be duplicated and translated separately from the original.

```html
<use xlink:href="#squiggle" transform="rotate(-90)
translate(-275)" x="0" y="125"></use>

```
It is important to note that the duplicated paths must still fit within the bounds of the `svg` `viewbox`; each `path` duplicated in this way is not a unique svg.  


*Thanks to [Brittany](https://github.com/boomingbrake) for showing me this trick - check out her [SVGs in action](http://codepen.io/Boomingbrake/pen/oxdgBj) on CodePen.*
