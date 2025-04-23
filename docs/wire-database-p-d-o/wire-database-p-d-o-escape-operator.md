Sanitize comparison operator
----------------------------

### Usage

    // basic usage
    $string = $database->escapeOperator(string $operator);
    
    // usage with all arguments
    $string = $database->escapeOperator(string $operator, $operatorType = 0, string $default = '=');

### Arguments

Name

Type(s)

Description

`operator`

string

`operatorType` (optional)

bool, int, null

Specify a WireDatabasePDO::operatorType\* constant (default=operatorTypeComparison)

`default` (optional)

string

Default/fallback operator to return if given one is not valid (default='=')

### Return value

`string`

