# Reflections

## Web Development

### Responsive Web Design Principles

#### CSS Flexbox

Justify Content
- To align and space out the flex-items in a certain way we use justify-content
``` 
syntax example
justify-content: center;
justify-content: flex-start;
justify-content: flex-end;
justify-content: space-between;
justify-content: space-around;
```

Align Items
- We can also use align elements using align-items property

```
values available similar to justify-content
align-items: center;
align-items: flex-start;
align-items: flex-end;
align-items: stretch;
align-items: baseline;
```

Flex-Wrap
- CSS flexbox has a feature to split a flex item into multiple rows (or columns). By default, a flex container will fit all flex items together. For example, a row will all be on one line. flex-wrap

- However, using the flex-wrap property, it tells CSS to wrap items. This means extra items move into a new row or column. The break point of where the wrapping happens depends on the size of the items and the size of the container.

- CSS also has options for the direction of the wrap:
```
nowrap: this is the default setting, and does not wrap items.

wrap: wraps items from left-to-right if they are in a row, or top-to-bottom if they are in a column.

wrap-reverse: wraps items from right-to-left if they are in a row, or bottom-to-top if they are in a column.
```

flex-shrink
- allows an item to shrink if the flex container is too small
- Items shrink when the width of the parent container is smaller than the combined width of all the flex item in it.
- takes number as values

```
    syntax
    flex-shrink: 1;
    flex-shrink: 3; <- shrinks three times as much as the other
```

flex-grow
- the opposite of flex-shrink

flex-basis
- property specifies the initial size of an item before CSS makes adjustment with flex-shrink or flex-grow

flex shorthand property
```
Example
 flex: 1 0 10px; 
 will set the item to flex-grow: 1;, flex-shrink: 0;, and flex-basis: 10px;.
```

we also have order property to rearrange items

```
order: 1 would be the first
order: 2 would be the second
```

align-self
- allows to adjust each item individually instead of setting them all at once
- accept same values as align-items


