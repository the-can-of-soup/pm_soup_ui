# Documentation

> [!IMPORTANT]
> DOCUMENTATION UNFINISHED

## Objects

Throughout this documentation, "object" will be defined as a value from the Objects extension of the structure
```JSON
{
    "type": ...,
    ...
}
```

Every object has a `type` key which should be a string representing the object's type. The rest of the keys will have a structure depending on the type.

## Widgets

SoupUI is based on an inheritance structure. You can think of it like a tree of nodes, where each node has one parent and zero or more children. The nodes in SoupUI are called "widgets", and the very top node is called the "top widget". These widgets are all stored in the `SoupUI: widgets` variable.

## Variables

These are the variables used by SoupUI. These variables are not intended to be directly modified.

### `SoupUI: stage size vector`
The size of the stage in pixels as a vector.

### `SoupUI: widgets`
The full state of the UI as a `soupui_widgets_list` object.
