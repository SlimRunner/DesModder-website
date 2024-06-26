---
title: Intellisense
eleventyNavigation:
  parent: DesModder
  title: Intellisense
  order: 1
---

## Documentation in Desmos

### Function Documentation

[See an example here.](https://www.desmos.com/calculator/3hkfwd6cqw)

DesModder Intellisense supports documentation for functions. Function documentation will appear while you are filling out the parameters for a function.

Put a text expression (either through the expression dropdown or by hitting the `"` key in an empty expression) directly before a function and put text in it to provide documentation for that function.

Function documentation can also contain rendered LaTeX mathematical expressions, which are enclosed by backticks (`\``). These use [Text Mode](../text-mode/) syntax. If an expression cannot be parsed as a Text Mode expression, it will fall back to being parsed as regular Desmos LaTeX.

### Parameter Documentation

You can provide documentation for specific function parameters by typing `@param PARAMNAME`, where `PARAMNAME` is the name of the function parameter as if it were written in [Text Mode](../text-mode/) format.

### Private and Public Expressions

- **Public expressions** are displayed in the intellisense menu.
- **Private expressions** are _not_ displayed in the intellisense menu.

- `@private`: All expressions are public by default. You can put `@private` in a text expression above an expression to make it a private expression. You can also use `@private` in the text for a folder to make every expression in that folder private. However, when making edits within the same folder, you will still see its contents in the intellisense menu. Think of it like a scoping system, with the folder as a scope.
- `@public`: Inside a folder marked as `@private`, you can make an expression public by placing a text expression immediately before it containing the string `@public`.

## Jump to Definition

Press `F9` while the text cursor (caret) is hovering over an identifier to jump to that identifier's definition. Alternatively, while the intellisense menu is open, you can click the compass button while hovering over an autocomplete suggestion to jump to its definition.

If there are multiple definitions, a menu listing them will open instead. Use the `Up` and `Down` arrow keys to navigate through this menu; and use `Enter` to select an option from it. Use `Escape` to close it.

## Autocomplete

Autocomplete can be controlled via mouse or keyboard.

- `Up` and `Down` arrows: Navigate through the autocomplete menu.
- `Enter`: Apply the selected autocomplete option.
- `Escape`: Disable the autocomplete menu until the next edit.

## Auto-Subscriptify

If this feature is enabled, then subscripts can be automatically inserted in some scenarios.

For example, if you have a function defined as `g_{ray}(x)=rgb(x,x,x)`, then you can directly write <kbd>g</kbd><kbd>r</kbd><kbd>a</kbd><kbd>y</kbd> to get `g_{ray}` without typing the underscore key <kbd>_</kbd>.

![](/img/auto_subscript_gray.png)
