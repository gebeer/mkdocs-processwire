Method called right before Inputfield markup is rendered, so that any dependencies can be loaded as well.
---------------------------------------------------------------------------------------------------------

Called before [`Inputfield::render()`](/api/ref/inputfield/render/) or [`Inputfield::renderValue()`](/api/ref/inputfield/render-value/) method by the parent [`InputfieldWrapper`](/api/ref/inputfield-wrapper/) instance. If you are calling either of those methods yourself for some reason, make sure that you call this `renderReady()` method first.

The default behavior of this method is to populate Inputfield-specific CSS and JS file assets into [`$config->styles`](/api/ref/config/styles/) and [`$config->scripts`](/api/ref/config/scripts/).

The return value is true if assets were just added, and false if assets have already been added in a previous call. This distinction probably doesn't matter in most usages, but here just in case a descending class needs to know when/if to add additional assets (i.e. when this method returns true).

### Usage

    // basic usage
    $bool = $inputfield->renderReady();
    
    // usage with all arguments
    $bool = $inputfield->renderReady($parent = null, bool $renderValueMode = false);

### Arguments

Name

Type(s)

Description

`parent` (optional)

`renderValueMode` (optional)

bool

Specify true only if this is for [`Inputfield::renderValue()`](/api/ref/inputfield/render-value/) rather than [`Inputfield::render()`](/api/ref/inputfield/render/).

### Return value

`bool`

True if assets were just added, false if already added.

