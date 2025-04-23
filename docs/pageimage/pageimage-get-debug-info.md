Verbose debug info (via
-----------------------

Available since version **3.0.132**.

### Usage

    // basic usage
    $array = $pageimage->getDebugInfo();
    
    // usage with all arguments
    $array = $pageimage->getDebugInfo(array $options = [], string $returnType = 'string');

### Arguments

Name

Type(s)

Description

`options` (optional)

array

The individual options you also passes with your image variation creation

`returnType` (optional)

string

'string'|'array'|'object', default is 'string' and returns markup or plain text

### Return value

`array` `object` `string`

