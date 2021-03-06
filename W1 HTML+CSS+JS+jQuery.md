# Week 1

## HTML
HTML = Hypertext Markup Language

### Headings

  Use headings as titles to introduce distinct sections. Headings come in 6 sizes starting with `h1`, `h2`, through `h6`. `h1` is the largest size, `h6` is the smallest
``` HTML
<h1>This is the largest heading</h1>
<h2>This is the second largest heading</h2>
<h6>This is the smallest heading</h6>
```

### Paragraphs

  Use paragraphs `p` to add long portions of text Paragraphs add vertical spacing between portions of text
``` HTML
<p>Lorem Ipsum is simply dummy text of the printing and typesetting
industry. Lorem Ipsum has been the industry's standard dummy text
ever since the 1500s, when an unknown printer took a galley of type
and scrambled it to make a type specimen book</p>
```

### Lists

  unordered list - `ul`, ordered list - `ol`, list item = `li`
``` HTML
<h2>Courses Spring 2018</h2>
<ul>
  <li>CS5610</li>
  <li>CS4500</li>
  <li>CS5200</li>
</ul>
<h2>Semesters</h2>
<ol>
  <li>Spring</li>
  <li>Summer 1</li>
  <li>Summer 2</li>
  <li>Fall</li>
</ol>
```

### Tables

  Use tables to display tabular data, their intended purpose, e.g. ,each row is a record, each column has same data types. Do not use tables to layout content. Use `div` and CSS instead
```HTML
<table>
  <thead></thead>
  <tbody></tbody>
</table>
```
  In both `thead` and `tbody`, we build up rows with `tr`. Under `tr` we use `td` to refer to each item
```HTML
<table border="1">
  <thead>
    <tr>
      <th>Username</th><th>Password</th><th>First Name</th>
      <th>&nbsp;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>alice</td> <td>*****</td> <td>Alice</td>
      <td>Wonderland</td> <td>Student</td> <td>Edit | Remove</td>
    </tr>
  </tbody>
</table>
```
  `&nbsp;` allows you to create multiple spaces that are visible on a web page and not only in the source code.

  Add attributes `rowspan=` or `colspan=` in `tr` expands the item to take up more than 1 space. `rowspan=2` means takes up 2 row, `colspan=3` means takes up 3 columns.

### Input fields and labels

  Attribute `for="usernameFld"` under `label` bounds this particular label with an input whose id is __usernameFld__. As a result, the action of clicking the lable is regared as clicking the input.

```HTML
<label for="usernameFld">
  Username
</label>
<input id="usernameFld"
  type="text"
  title="Username"
  placeholder="alice" />

<label for="firstNameFld">
  First Name
</label>
<input
  id="firstNameFld"
  value="Alice" />
```
Attribute `type="date"` helps display a date selector.
```HTML
<label for="dobFld">
  Date of Birth
</label>
<input
  type="date"
  id="dobFld"
  value="2011-11-22" />
```

### Dropdowns with select
```HTML
<select name="role">
  <option value="FACULTY">
    Faculty
  </option>
  <option value="STUDENT">
    Student
    </option>
  <option value="ADMIN">
  Admin
  </option>
</select>
```

### BUTTONS, RADIOS & CHECKBOXES

  buttons:

```HTML
<button type="button">
  Delete
</button>
<button type="button">
  Edit
</button>
<button type="submit">
  Update
</button>
```

Checkbox and radio buttons:
```HTML
<label>
  <input name="b" type="checkbox"/> Tenured
</label>
<label>
  <input name="a" type="radio"/> Yes
</label>
<label>
  <input name="a" type="radio" checked/> No
</label>
```


## JavaScript

### fetch
[Detailed Descrptions](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch)

#### Simplest fetch example:
```JavaScript
const url = 'http://example.com/movies.json'
fetch(url)
  .then(function(response){
    return response.json();
  })
  .then(function (myJson){
    console.log(JSON.stringify(myJson))
  })
```
This example returns a json object from given url.

#### Uploading JSON data:
```JavaScript
const url = 'http://example.com/profile'
const jsonData = {username : 'example'}
fetch(url, {
  method: 'POST', // or 'PUT'
  body: JSON.stringify(jsonData)
  headers : {
    'content-type' : 'application/json'
    }
  }).then(function (response){
    return response.json())
  })
```
