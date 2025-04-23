Disable the given log name temporarily so that save() calls do not record entries during this request
-----------------------------------------------------------------------------------------------------

Available since version **3.0.148**.

### Usage

    $self = $log->disable(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

Log name or specify '\*' to disable all

### Return value

`self`

### See Also

*   [WireLog::enable()](/api/ref/wire-log/enable/)

