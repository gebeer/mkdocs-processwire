Load the given page field from the database table and return the value.
-----------------------------------------------------------------------

*   Return NULL if the value is not available.
*   Return the value as it exists in the database, without further processing.
*   This is intended only to be called by Page objects on an as-needed basis.
*   Typically this is only called for fields that don't have 'autojoin' turned on.
*   Any actual conversion of the value should be handled by the [`Fieldtype::wakeupValue()`](/api/ref/fieldtype/wakeup-value/) method.

### Usage

    $mixed = $fieldtype->loadPageField(Page $page, Field $field);

### Arguments

Name

Type(s)

Description

`page`

Page

Page object to save.

`field`

Field

Field to retrieve from the page.

### Return value

`mixed` `null`

