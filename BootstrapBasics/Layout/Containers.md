# Containers
> Containers are the most basic layout element in Bootstrap that 
    
    1. wrap site contents, pad
    2. sometimes center the content within them
    3. align your content within a given device or viewpoint
    4. and house our grid system
Containers can also be nested. 

**Bootstrap comes with three diffrent containers:**

* ```.container```, which sets a max-width at each responsive breakpoint
* ```.container-{breakpoint}```, which is width: 100% until the specified breakpoint

* ```.container-fluid```, which is width: 100% at all breakpoints

The table illustrates how each container's max-width compares to the original ```.container``` and ```.container-fluid``` across each breakpoint.


|                |Extra small <576px|Small ≥576px|Medium ≥768px|Large ≥992px|X-Large ≥1200px |XX-large ≥1400px|
|----------------|------------------|------------|-------------|------------|----------------|----------------|       
|.container	     | 100%	            | 540px  	 | 720px	   | 960px	    | 1140px	     | 1320px         |
|.container-sm	 | 100%	            | 540px	     | 720px	   | 960px	    | 1140px	     | 1320px         |
|.container-md	 | 100%	            | 100%	     | 720px	   | 960px	    | 1140px	     | 1320px         |
|.container-lg	 | 100%	            | 100%	     | 100%	       | 960px	    | 1140px	     | 1320px         |
|.container-xl	 | 100%	            | 100%	     | 100%	       | 100%	    | 1140px	     | 1320px         |
|.container-xxl	 | 100%             | 100%	     | 100%	       | 100%	    | 100%	         | 1320px         |
|.container-fluid|	100%	        | 100%	     | 100%	       | 100%	    | 100%	         | 100%           |

<br />

## Default container
---
> Bootstrap's defailt ```.containers``` class is a responsive, fixed-width container, meaning its ```max-width``` changed at each breakpoint.

```HTML
    <div class="container">
        <!-- Content Here -->
    </div>
```

<br />

## Responsive containers
---

> Responsive containers allow to specify a class that is 100% wide until the specified breakpoint is reached, after which we apply ```max-widths``` for each of the higher breakpoints.

For example ```.container-sm``` is 100% wide to start until the ```sm``` breakpoint is reached, where it will sccale up with ```md```, ```lg```,```xl,``` and ```xxl```.
<br />

```HTML
    <div class="container-sm">100% wide until small breakpoint</div>
    <div class="container-md">100% wide until medium breakpoint</div>
    <div class="container-lg">100% wide until large breakpoint</div>
    <div class="container-xl">100% wide until extra large breakpoint</div>
    <div class="container-xxl">100% wide until extra extra large breakpoint</div>
```
<br />

## Fluid Containers
---
> ```.container-fluid``` creates a full width container, spanning the entire width of the viewport.

```HTML
    <div class="container-fluid">
        ...
    </div>
```
<br />

## Sass
> Bootstrap generates a series of predefined container classes to help build different layout, which can be customized by modifying the __Sass map__ ( found in ```.variable.scss```) that powers them:

```CSS
$container-max-widths: (
  sm: 540px,
  md: 720px,
  lg: 960px,
  xl: 1140px,
  xxl: 1320px
);
```

We can also create containers with __Sass mixin__.
```CSS
//Source mixin
@mixin make-container($padding-x: $container-padding-x){
    width: 100%;
    padding-right: $padding-x;
    padding-left: $padding-x;
    margin-right: auto;
    margin-left: auto;
}

//Usage 
.custom-container{
    @include make-container();
}
```
<br />

[previous page>>](GridSystem.md.md)       <br /> [next page>>](Rows.md)
