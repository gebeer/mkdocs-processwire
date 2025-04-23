Return a new copy of this WireArray with the given item(s) appended
-------------------------------------------------------------------

Primarily for syntax convenience in fluent interfaces.

### Example

    if($page->parents->and($page)->has($featured)) { 
      // either $page or its parents has the $featured page
    }

### Usage

    $items = $wireArray->and($item);

### Arguments

Name

Type(s)

Description

`item`

Wire, WireArray

Item(s) to append

### Return value

[`WireArray`](/api/ref/wire-array/)

New WireArray containing this one and the given item(s).

