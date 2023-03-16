# Bootstrap Grid System
Bootstrap includes a responsive, fluid grid system that allows upto 12 columns across the page. We can use these 12 columns each of width 1, or use 4 columns each of width 3 or any other combination individually or merge them together for wider columns or all combinations of values summing up to 12 as the
device or viewport size increases. It includes predefined classes for easy layout options, as well as powerful mixins
for generating more semantic layouts.

<br />
 The following is a basic structure of a Bootstrap Grid:

```html
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>
<div class="row">
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
  <div class="col-*-*"></div>
</div>
<div class="row">
  ...
</div>
```
>First; create a row (\<div class="row">). Then, add the desired number of columns (tags with appropriate .col-*-* classes). Note that numbers in .col-*-* should always add up to 12 for each row.

<br/>

![Grid System](https://media.geeksforgeeks.org/wp-content/uploads/Bootstrap-part-2.png)

<br />

## Grid Classes:
---
> Bootstrap grid system has four classes that can be combined to make more flexible layouts:

* xs (<576px): For Portrait Mobile Phones.
* sm (>=576px): For Landscapes phones
* md (>=768px): For Tablets/Phablets
* lg (>=992px): For Small-sized Desktops/Laptops
* xl (>=1200px): For Larger-sized Desktops/Laptops

<br />

## Components of Grid System
1. [Containers](Containers.md)
1. [Rows]()
1. [Columns]()
1. [Column Resets]()
1. [Column Offset]()
1. [Nesting Columns]() 

# Grid System Rules
Some Bootstrap grid system rules:

* Rows must be placed within a ```.container``` (fixed-width) or ```.container-fluid``` (full-width) for proper alignment and padding

* Use rows to create horizontal groups of columns

* Content should be placed within columns, and only columns may be immediate children of rows

* Predefined classes like ```.row``` and ```.col-sm-4``` are available for quickly making grid layouts

* Columns create gutters (gaps between column content) via padding. That padding is offset in rows for the first and last column via negative margin on ```.rows```

* Grid columns are created by specifying the number of 12 available columns you wish to span. For example, three equal columns would use three ```.col-sm-4```

* Column widths are in percentage, so they are always fluid and sized relative to their parent element

<br /><br />

[previous page>>](../Introduction.md)     <br /> [next page>>](Containers.md)
