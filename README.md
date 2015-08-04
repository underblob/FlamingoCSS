# Flamingo CSS

**Flamingo CSS** is a simple responsive fluid grid framework. It has two responsive breakpoints for tablet (1250px)
and mobile (770px). The CSS grid has 12 columns rendered by default. SASS variables are easily updated to set the number of column classes rendered in the CSS or to adjust the responsive breakpoints.

## Example usage

Grid containers should be wrapped in `.flg-row`. 

Grid containers should contain the `.flg` class as well as a column width definition. Column widths are defined similar to fractions. eg, you have 4 columns and want to occupy 3 of the 4. As a fraction, this would read "3/4". As an html container, the Flamingo class would read `.flg-3-4`.

For tablet or mobile widths, include the `tab-` or `mob-` identifiers. eg, `.flg-mob-1-1` would make the container 100% wide when the viewport hits 770px or narrower.

```
<div class="flg-row">
  <div class="flg flg-1-4 flg-tab-1-1">[ ... ]</div>
  <div class="flg flg-3-4 flg-tab-1-1">[ ... ]</div>
</div>
```

## Browser Compatibility

Flamingo uses the `box-sizing` CSS property, which is not available on all browsers. For compatibility matrix, see
[Can I use](http://caniuse.com/#feat=css3-boxsizing)

## Customizing the Framework

The framework can be customized for a smaller footprint if not all 12 columns are desired or if more than 12 columns are required for your layout. To do this, you will need to have SASS gem running locally. For details on how to do this, see the [Compass instructions](http://compass-style.org/install/). 

* With Compass/SASS is running, update the `$total-cols` variable in `flg.scss` to the desired number of grid columns. 
* Once you have made changes to `flg.scss`, open a command prompt and cd to the repo on your local workstation and render the CSS using `compass compile`:
```
> cd \Source\Github\FlamingoCSS
> compass compile
```

To update the responsive breakpoints, edit the `$media-tablet` and `$media-mobile` variables and then compile the CSS using `compass compile` as described above.

If you don't want to spin up SASS on your local workstation, you can change the responsive breakpoints in the CSS file. Just look for the two big comment blocks that start the tablet and mobile style sections and edit the `@media` queries directly beneath them: 
```
/*	================================================================================ */
/*	Responsive layouts for tablet. */
/*	================================================================================ */
@media only screen and (max-width: 1250px) {
[ ... ]
/*	================================================================================ */
/*	Responsive layouts for mobile. */
/*	================================================================================ */
@media only screen and (max-width: 769px) { 
[ ... ]
```
