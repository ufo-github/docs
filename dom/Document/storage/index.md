---
title: 'storage'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, compat, better spec link'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
tags:
  - Events
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/Document/storage

---
## Overview Table

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
 ?

</td>
</tr>
</table>
## Notes

### Remarks

The [**URL**](/dom/Window/URL) property specifies the URL of the Web page that made the update. For Windows Internet Explorer 9 standards mode, **onstorage** will only fire on window objects. Handlers attached to document.body or document objects will not receive the event. (Note this does not apply to the [**storagecommit**](/dom/Document/storagecommit) event.) The **onstorage** event will only fire on window objects. Handlers attached to document.body or document objects will not receive the event. (Note this does not apply to the [**storagecommit**](/dom/Document/storagecommit) event.) The **onstorage** event is specified in the W3C [Web Storage](http://go.microsoft.com/fwlink/?LinkId=217507) specification. To invoke this event, do one of the following:

-   Set or update a session or local storage value with [**setItem**](/apis/web-storage/Storage/setItem).
-   Remove a session or local storage value with [**removeItem**](/apis/web-storage/Storage/removeItem).

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   `frameSet`
-   `window`
-   `Introduction to Web Storage`
