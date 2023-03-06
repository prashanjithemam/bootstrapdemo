# Grid System

> Bootstrap Grid System allows upto 12 columns across the page.We can use each of them      
     1.individually or merge them together for wider columns.
     \
     \
     2.all combinations of values summing up to 12. 
     \
     \
We can use 12 columns each of width 1, or use 4 columns each of width 3 or any other combination.

<br/>

![Grid System](https://media.geeksforgeeks.org/wp-content/uploads/Bootstrap-part-2.png)

<br /><br />

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


## Min-width
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
