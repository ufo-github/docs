---
title: 'text-decoration-overline'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: text-decoration-overline
  topic: css
notes:
  - 'Needs summary, spec reference, standardization status, fix table coding in Notes, fix broken link'
overview_table:
  '[Initial value](/css/concepts/initial_value)': ''
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': ''
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': ''
readiness: 'In Progress'
tags:
  - CSS_Properties
  - CSS
  - Needs_Summary
uri: css/properties/text-decoration-overline

---
## Overview table

[Initial value](/css/concepts/initial_value)
:

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:

## Syntax

-   `text-decoration-overline: VARIANT_FALSE`
-   `text-decoration-overline: VARIANT_TRUE`

## Values

VARIANT\_TRUE
:   A line is drawn over the text.

VARIANT\_FALSE
:   A line is not drawn over the text.

## Examples

This example uses the **textDecorationOverline** property to draw a line over the text when the user moves the mouse over the text.

``` html
<P onmouseover="this.style.textDecorationOverline=true;">
Mouse over this text for an overline.
</P>
```

### Syntax

`textDecorationOverline: VARIANT_TRUE | VARIANT_FALSE`

### Requirements

{

## See also

### Related pages

-   defaultSelected[defaultSelected](/dom/HTMLOptionElement/defaultSelected)
-   runtimeStyle[runtimeStyle](/css/cssom/runtimeStyle)
-   style[style](/css/cssom/style)
-   textDecoration[textDecoration](/css/properties/text-decoration)
