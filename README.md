# Flamingo CSS

**Flamingo CSS** is a simple responsive fluid grid framework. It has two responsive breakpoints for tablet (1250px)
and mobile (770px). The CSS grid has 12 columns rendered by default but the SASS is configurable if a smaller
footprint is desired.

The SASS can be updated to render as many or as few columns that you need by simply updating the `$total-cols` variable.

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
