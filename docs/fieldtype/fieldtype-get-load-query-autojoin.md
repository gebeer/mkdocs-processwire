Return the query used for Autojoining this field (if different from getLoadQuery) or NULL if autojoin not allowed.
------------------------------------------------------------------------------------------------------------------

### Usage

    $databaseQuerySelect = $fieldtype->getLoadQueryAutojoin(Field $field, DatabaseQuerySelect $query);

### Arguments

Name

Type(s)

Description

`field`

Field

`query`

DatabaseQuerySelect

### Return value

`DatabaseQuerySelect` `null`

