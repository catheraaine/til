## Forms: Option Groups

For my [RISK Legacy App](https://github.com/catheraaine/risk-legacy), I needed to create a `select` item that had dozens of country names for options, all in one long list. Here's how that looks:

```html
  <select>
    <option>Afghanistan</option>
    <option>China</option>
    <option>India</option>
    <option>Great Britain</option>
    <option>Iceland</option>
    <option>Russia</option>
  </select>

```
A better way is to group the countries into continents, which increases readability within the drop down menu. This is done with the `<optgroup>` tag.

```html
  <select>
    <optgroup label="Asia">
      <option>Afghanistan</option>
      <option>China</option>
      <option>India</option>
    </optgroup>
    <optgroup label="Europe">
    <option>Great Britain</option>
    <option>Iceland</option>
    <option>Russia</option>
    </optgroup>
  </select>
```
Here's the select box in action, check out the neat nesting labels provided by `optgroup`:

![DropDown Box](http://res.cloudinary.com/catheraaine/image/upload/v1460404725/Screen_Shot_2016-04-11_at_3.57.53_PM_brmxk9.png)
