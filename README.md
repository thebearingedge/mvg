# mvg

Minimum Viable Grid. Uses the classic floating 12-column system.

```stylus
$units  = 12
$gutter = 1.5rem
```

## Breakpoints

```stylus
@media screen and (max-width: 48rem)
  columns('xs')

@media screen and (min-width: 48rem)
  columns('sm')

@media screen and (min-width: 62rem)
  columns('md')

@media screen and (min-width: 74rem)
  columns('lg')
```

## Grid

The `.grid` provides a container with a restricted width. The width of the `.grid` snaps to accommodate the viewport as it expands through breakpoints. The `.grid-fluid` class flows to the full width of its parent element.

## Row

A `.row` is used to house floating column elements, ensuring that they flow to the full width of the grid. Groups of columns are stacked within `.row`s.

## Column

Like many classic CSS grids, `mvg` provides a range of `.col` classes with the format `.col-(xs|sm|md|lg)-(1-12)`. All `.col`s expand to the full width of their parent `.row` until their corresponding breakpoint is reached. For instance, `.col-md-4` will be full-width until the viewport reaches a "medium" width, in which case it will be restricted to the next available 4 of 12 column "units".

## Offset

Empty columns may be omitted with the use of `.offset` classes. Adding an `.offset` to a column with increase its margins to consume the leftward number of column "units" specified.

## Example

```html
<div class="grid">
  <div class="row">
    <div class="col-md-2">Lorem ipsum dolor sit amet</div>
    <div class="col-md-4">Lorem ipsum dolor sit amet</div>
    <div class="col-md-6">Lorem ipsum dolor sit amet</div>
  </div>
  <div class="row">
    <div class="col-md-4 col-md-offset-8">Lorem ipsum dolor sit amet</div>
  </div>
</div>
```
