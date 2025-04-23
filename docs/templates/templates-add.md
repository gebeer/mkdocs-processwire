Add and save new template (and fieldgroup) with given name and return it
------------------------------------------------------------------------

Available since version **3.0.170**.

### Usage

    // basic usage
    $template = $templates->add(string $name);
    
    // usage with all arguments
    $template = $templates->add(string $name, array $properties = []);

### Arguments

Name

Type(s)

Description

`name`

string

`properties` (optional)

array

Any additional properties to add to template

### Return value

[`Template`](/api/ref/template/)

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if given invalid template name or template already exists
    

