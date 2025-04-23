Is the given string a database comparison operator?
---------------------------------------------------

### Example

    if($database->isOperator('>=')) {
      // given string is a valid database operator
    } else {
      // not a valid database operator
    }

### Usage

    // basic usage
    $bool = $database->isOperator(string $str);
    
    // usage with all arguments
    $bool = $database->isOperator(string $str, $operatorType = 2, bool $get = false);

### Arguments

Name

Type(s)

Description

`str`

string

1-2 character operator to test

`operatorType` (optional)

bool, null, int

Specify a WireDatabasePDO::operatorType\* constant (3.0.162+), or any one of the following (3.0.143+):

*   `NULL`: allow all operators (default value if not specified)
*   `FALSE`: allow only comparison operators
*   `TRUE`: allow only bitwise operators

`get` (optional)

bool

Return the operator rather than true, when valid? (default=false) Added 3.0.162

### Return value

`bool`

True if valid, false if not

