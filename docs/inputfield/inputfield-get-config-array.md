Alternative method for configuration that allows for array definition
---------------------------------------------------------------------

*   This method is typically used instead of the [`Inputfield::getConfigInputfields`](/api/ref/inputfield/get-config-inputfields/) method for module authors that prefer to use the array definition.
    
*   If both `getConfigInputfields()` and `getConfigArray()` are implemented, both will be used.
    
*   See comments for [`InputfieldWrapper::importArray()`](/api/ref/inputfield-wrapper/import-array/) for example of array definition.
    

### Example

    // Example implementation
    public function ___getConfigArray() {
      return [
        'test' => [
          'type' => 'text',
          'label' => 'This is a test',
          'value' => 'Test'
        ]
      ];
    );

### Usage

    $array = $inputfield->getConfigArray();

### Return value

`array`

