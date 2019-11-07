# A Mobile First Responsive Grid 

For example purposes, I have created a mobile-first responsive grid. It is large, 16 columns - a 12 column grid should work in most cases. My rational for choosing the large number of columns is so the grid will be substantially reduced if it is going to be used for any assessed work.

## Getting Started

Simply clone this repository and point your browser at the `index.html` file. 

## An example

```html
<div class="wrapper">
    <div class="row">
    <div class="col-16 col-sm-4 offset-sm-6 nav">
        <ul>
          <li><a href="#"> Home </a></li>
          <li><a href="#"> Contact </a></li>
          <li><a href="#"> About </a></li>
        </ul>
    </div>
</div>
```

In the above example, I have set up a full-width grid for mobile devices (`col-16`), which snaps to a 4 column  grid with a 6 column offset on slightly larger devices (`col-sm-4` `offset-sm-6`). If we did not apply the  `col-sm-4` class, our grid would remain 16 cols on any viewport size. However, as it stands, our grid on a viewport larger than `540px` (our sm breakpoint) will become two columns. This view will remain true unless we add a `col-` class that activates at a new, larger, breakpoint (e.g. `col-md-`).  

I find the mobile-first approach demonstrated above an excellent way to work. Broadly speaking, my workflow is as follows:

- First, I lay out the mobile version of the site 
- Next, I gradually increase the viewport until things looks wrong   
- I then tweak the number of columns to fix the layout
- I then simply repeat the process, gradually increasing the viewport until a further readjustment is needed 

## How the Grid System Works

My solution is perhaps a little clunky. I simply re-define the grid, in its entirety, within a media query with a new `col` name representative of the breakpoint that media query has created.

```css 
@media (min-width: 540px) {
  .col-sm-1 {
      width: 6.25%;
      
    }
    
    .col-sm-2  {
      width: 12.5%;
    } 
    
    ....
}
```


## Your Task

This grid is only part finished, you taks us to convert it to a 12-col grid and finish off the grid. There are still a few questions that need to be addressed:

- How can we convert this grid to `12-cols`?
- How can we support further viewport sizes (e.g. medium, large and extra large)?
  - What should we set the breakpoints to?
- What `max-width` should `.wrapper` be on different viewports?
- Can columns be nested?
- What further features should we add to make the grid as flexible as possible?
  - e.g. could we have `.wrapper-sm` ,`.wrapper-md` and `.wrapper-lg`  to give us flexibility on how our content can be constrained?
- **Bonus Task:** How can we significantly reduce the amount of css using [sass](https://www.npmjs.com/package/sass)?





 
