Format the given text string with Page and Field provided.
----------------------------------------------------------

Module developers may override this function completely when providing your own text formatter. No need to call the parent.

### Usage

    $textformatter->formatValue(Page $page, Field $field, $value);

### Arguments

Name

Type(s)

Description

`page`

Page

`field`

Field

`value`

string, mixed

Value is provided as a reference, so is modified directly (not returned).

