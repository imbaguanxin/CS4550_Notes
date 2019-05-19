# Week 1

## HTML
HTML = Hypertext Markup Language

1. Headings

  Use headings as titles to introduce distinct sections. Headings come in 6 sizes starting with `h1`, `h2`, through `h6`. `h1` is the largest size, `h6` is the smallest
``` HTML
<h1>This is the largest heading</h1>
<h2>This is the second largest heading</h2>
<h6>This is the smallest heading</h6>
```

2. Paragraphs

  Use paragraphs `p` to add long portions of text Paragraphs add vertical spacing between portions of text
``` HTML
<p>Lorem Ipsum is simply dummy text of the printing and typesetting
industry. Lorem Ipsum has been the industry's standard dummy text
ever since the 1500s, when an unknown printer took a galley of type
and scrambled it to make a type specimen book</p>
```

3. Lists

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

4. Tables

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



5.
