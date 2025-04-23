Get the root parent InputfieldWrapper element (farthest parent, commonly InputfieldForm)
----------------------------------------------------------------------------------------

This returns null only if Inputfield it is called from has not yet been added to an InputfieldWrapper.

Available since version **3.0.106**.

### Usage

    $inputfieldForm = $inputfield->getRootParent();

### Return value

`InputfieldForm` [`InputfieldWrapper`](/api/ref/inputfield-wrapper/) `null`

