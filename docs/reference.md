# SoupUI Reference

[← Back to documentation home](https://github.com/the-can-of-soup/pm_soup_ui/blob/main/docs/main.md)

> [!IMPORTANT]
> DOCUMENTATION UNFINISHED

## Objects

Throughout this documentation an "object" is defined as a value from the Objects extension of the structure:
```
{
    "type": <[String] object type>,
    ...
}
```

A "generic object" is defined as *any* value from the Objects extension, including objects:
```
{
    ...
}
```

Every object has a `type` key which should be a string representing the object's type. The rest of the keys will have a structure depending on the type.

Whenever a data structure is documented, keys or values in angled brackets `<>` are placeholders. The part enclosed in square brackets `[]` is the expected type, and the rest is the description of the placeholder. The following table shows what each placeholder type means:

| Type              | Meaning                                           | Examples                                  |
|-------------------|---------------------------------------------------|-------------------------------------------|
| `String`          | A string.                                         | `"foo"`, `"Hello, World!"`                |
| `Number`          | A float or integer.                               | `0.5`, `-3`, `NaN`, `Infinity`            |
| `Boolean`         | `true` or `false`.                                | `true`, `false`                           |
| Other             | An object of the type given.                      | `{"type": "soupui_widget_id", "id": 4}`   |

In data structure documentation, `...` in an array means the array may have any number of values structured like the last value listed. For example:
```
[
    <[String] the name of the randomizer log>,
    {
        "seed": <[Number] the seed before random() was called>,
        "time": <[Number] the value of the timer when random() was called>
    },
    ...
]
```
The above structure defines an array starting with a string, and then containing any number of elements following the structure of the generic object shown.

In data structure documentation, `...` in a generic object means the generic object may have number of key-value pairs structured like the last pair listed. For example:
```
{
    "sprite_count": <[Number] the number of sprites>,
    <[String] the name of the sprite>: <[Boolean] whether the sprite should be visible>,
    ...
}
```
The above structure defines a generic object starting with a `sprite_count` key, and then containing any number of key-value pairs following the structure of the second pair shown.

## Object Types

These are the object types used by SoupUI.

### `soupui_widget_id`


## Variables

These are the variables used by SoupUI. These variables are not intended to be directly modified.

### `SoupUI: stage size vector`
The size of the stage in pixels as a vector.

### `SoupUI: widgets`
The full state of the UI as a `soupui_widgets_list` object.
