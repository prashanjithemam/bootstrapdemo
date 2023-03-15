# Breakpoints
> Breakpoints are customizable widths that determine how your responsive layout can be adapted across device or viewport sizes in Bootstrap.

<br />
Bootstrap includes six default breakpoints, sometimes referred to as grid tiers, for building responsively. <br />

<br />

| Breakpoints            | Class Infinix       | Dimensions     |
|------------------------|---------------------|----------------|
| Extra small            | none                | <576px         |
| Small	               | sm	                 | ≥576px         |
| Medium	               | md	                 | ≥768px         |
| Large	               | lg	                 | ≥992px         | 
| Extra large	          | xl	                 | ≥1200px        |
| Extra extra large	     | xxl	            | ≥1400px        |

<br /><br />

# Media Queries
> Media queries are a feature of CSS that allow you to conditionally apply styles based on a set of browser and operating system parameters. We most commonly use min-width in our media queries.<br />


## Min-width<br />

> Bootstrap primarily uses the following media query ranges—or breakpoints—in our source Sass files for our layout, grid system, and components.
```css
     // Source mixins

          // No media query necessary for xs breakpoint as it's effectively `@media (min-width: 0) { ... }`
          @include media-breakpoint-up(sm) { ... }
          @include media-breakpoint-up(md) { ... }
          @include media-breakpoint-up(lg) { ... }
          @include media-breakpoint-up(xl) { ... }
          @include media-breakpoint-up(xxl) { ... }

          // Usage

          // Example: Hide starting at `min-width: 0`, and then show at the `sm` breakpoint
          .custom-class {
          display: none;
          }
          @include media-breakpoint-up(sm) {
          .custom-class {
          display: block;
          }
          }
```
These Sass mixin translate in our compiled CSS using the values declared in our Sass variable. For example:

```CSS
     // X-Small devices (portrait phones, less than 576px)
     // No media query for `xs` since this is the default in Bootstrap

     // Small devices (landscape phones, 576px and up)
     @media (min-width: 576px) { ... }

     // Medium devices (tablets, 768px and up)
     @media (min-width: 768px) { ... }

     // Large devices (desktops, 992px and up)
     @media (min-width: 992px) { ... }

     // X-Large devices (large desktops, 1200px and up)
     @media (min-width: 1200px) { ... }

     // XX-Large devices (larger desktops, 1400px and up)
     @media (min-width: 1400px) { ... }
```
## Max-width
> We occasionaly use media queries that go inthe other direction (the given screen size or smaller):<br />

```CSS
     // No media query necessary for xs breakpoint as it's effectively `@media (max-width: 0) { ... }`
     @include media-breakpoint-down(sm) { ... }
     @include media-breakpoint-down(md) { ... }
     @include media-breakpoint-down(lg) { ... }
     @include media-breakpoint-down(xl) { ... }
     @include media-breakpoint-down(xxl) { ... }

     // Example: Style from medium breakpoint and down
     @include media-breakpoint-down(md) {
     .custom-class {
     display: block;
     }
     }
```

These mixins take those declared breakpoints, subtract .02px from the, and use them as our max-width values. For example:

```CSS
     // `xs` returns only a ruleset and no media query
     // ... { ... }

     // `sm` applies to x-small devices (portrait phones, less than 576px)
     @media (max-width: 575.98px) { ... }

     // `md` applies to small devices (landscape phones, less than 768px)
     @media (max-width: 767.98px) { ... }

     // `lg` applies to medium devices (tablets, less than 992px)
     @media (max-width: 991.98px) { ... }

     // `xl` applies to large devices (desktops, less than 1200px)
     @media (max-width: 1199.98px) { ... }

     // `xxl` applies to x-large devices (large desktops, less than 1400px)
     @media (max-width: 1399.98px) { ... }   
```
> _Browsers don’t currently support range context queries, so we work around the limitations of min- and max- prefixes and viewports with fractional widths (which can occur under certain conditions on high-dpi devices, for instance) by using values with higher precision._
<br/>

## Single Breakpoint
---
<br />

> Single breakpoints are  media queries and mixins for targeting a single segmment of screen sizes using the minimum and maximum breakpoint widths.

```CSS
     @include media-breakpoint-only(xs) { ... }
     @include media-breakpoint-only(sm) { ... }
     @include media-breakpoint-only(md) { ... }
     @include media-breakpoint-only(lg) { ... }
     @include media-breakpoint-only(xl) { ... }
     @include media-breakpoint-only(xxl) { ... }
```

For example
```CSS
@include media-breakpoint-only(md) {... } 
```
will result in:

```CSS
     @media (min-width: 768px) and (max-width: 991.989px) { ... }
```
## Between Breakpoints
> Similarly, media queries may span multiple breakpoint widths:

```CSS
     @include media-breakpoint-between(md,x1) { ... }
```
Which will result in:
```CSS
     //Example
     //Apply styles starting from medium devices and upto extra large devices  
     @media(min-width: 768px) and (max-width:1199.98px) { ... }
```

[previous page>>](Containers.md)     <br /> [next page>>](Containers.md)
