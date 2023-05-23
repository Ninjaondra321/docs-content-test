
TODO: sem dopiš ukázku

## Structure
``` html
<table class="hover centered striped">
  <thead>
    <tr>
      <th>Firstname</th>
      <th>Lastname</th>
      <th>Age</th>
      <th>Action</th>
      <th>Icon</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>Doe</td>
      <td>24</td>
      <td><button class="btn primary">Click</button></td>
      <td>
        <p class="g-icon large">search</p>
      </td>
    </tr>
    <tr>
      <td>Ben</td>
      <td>Smith</td>
      <td>25</td>
      <td><button class="btn primary">Click</button></td>
      <td>
        <p class="g-icon large"> phone </p>
      </td>
    </tr>
    <tr>
      <td>John</td>
      <td>Dooe</td>
      <td>18</td>
      <td><button class="btn primary">Click</button></td>
      <td>
        <p class="g-icon large"> mail </p>
      </td>
    </tr>
  </tbody>
</table>
```
## Options
### Stripped
just add table.stripped
### Highlight on hover
just add table.hover
### Compact
just add table.compact


## Design guidelines
``` css
table.striped tbody tr:nth-child(odd) {
    background-color: /* Add your style here*/;
}

table.hover tbody tr:hover {
    background-color: /* Add your style here*/ !important;
}
  
table thead {
    border-bottom: /* Add your style here*/;
}
  
table tr {
    border-bottom: /* Add your style here*/;
}
```

## Part from BEŠAMEL
``` css
TODO!
```
