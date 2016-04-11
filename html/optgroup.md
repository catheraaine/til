## Forms: Option Groups

HTML forms may be highly common, but I am still learning how to use them.

Today, I created a `select` list that had dozens of country names for options, all in one long list.

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
A better option is to group the countries into continents, which increases readability within the drop down menu. This is done with the `<optgroup>` tag.

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
