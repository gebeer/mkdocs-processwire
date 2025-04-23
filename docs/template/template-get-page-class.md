Get class name to use for Page objects using this template
----------------------------------------------------------

Note that value can be different from the `$template->pageClass` property, since it is determined at runtime. If it is different, then it is at least a class that extends the one defined by the pageClass property.

Available since version **3.0.152**.

### Usage

    // basic usage
    $string = $template->getPageClass();
    
    // usage with all arguments
    $string = $template->getPageClass(bool $withNamespace = true);

### Arguments

Name

Type(s)

Description

`withNamespace` (optional)

bool

Returned class includes namespace? (default=true)

### Return value

`string`

Returned page class includes namespace

