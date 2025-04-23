Enable a previously disabled log
--------------------------------

Available since version **3.0.148**.

### Usage

    $self = $log->enable(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

Log name or specify '_' to reverse a previous disable('_') call.

### Return value

`self`

### See Also

*   [WireLog::disable()](/api/ref/wire-log/disable/)

