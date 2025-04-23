Given a selector, return whether or not this Page matches using runtime/memory comparison
-----------------------------------------------------------------------------------------

### Example

    if($page->matches("created>=" . strtotime("today"))) {
      echo "This page was created today";
    }

### Usage

    $bool = $page->matches($s);

### Arguments

Name

Type(s)

Description

`s`

string, Selectors, array

Selector to compare against (string, Selectors object, or array).

### Return value

`bool`

Returns true if this page matches, or false if it doesn't.

