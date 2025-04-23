Return template label for current language, or specified language if provided
-----------------------------------------------------------------------------

If no template label, return template name. This is different from `$template->label` in that it knows about languages (when installed) and it will always return something. If there's no label, you'll still get the name.

### Usage

    // basic usage
    $string = $template->getLabel();
    
    // usage with all arguments
    $string = $template->getLabel($language = null);

### Arguments

Name

Type(s)

Description

`language` (optional)

Page, Language

Optional, if not used then user's current language is used

### Return value

`string`

