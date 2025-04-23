Given a selector, return whether or not this Page matches by querying the database
----------------------------------------------------------------------------------

Available since version **3.0.225**.

### Example

    if($page->matchesDatabase("created>=today")) {
      echo "This page was created today";
    }

### Usage

    $bool = $page->matchesDatabase($s);

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

