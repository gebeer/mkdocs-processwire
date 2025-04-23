Is the current request of the specified type?
---------------------------------------------

This is a more readable/shorter alias of [`$input->requestMethod('type')`](/api/ref/input/request-method/) for syntax convenience. Internally, it determines the request type without accessing any input data, so it is efficient.

Available since version **3.0.145**.

### Example

    // The following are equivalent:
    $isPost = $input->is('post');
    $isPost = $input->requestMethod('post');

### Usage

    $bool = $input->is(string $method);

### Arguments

Name

Type(s)

Description

`method`

string

Specify one of: post, get, head, put, delete, options, patch (not case sensitive)

### Return value

`bool`

