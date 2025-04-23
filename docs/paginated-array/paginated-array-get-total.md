Get the total number of items in the WireArray, including all paginations.
--------------------------------------------------------------------------

If no limit is used, this returns total number of items currently in the WireArray, which would be the same as the [`WireArray::count()`](/api/ref/wire-array/count/) value. But when a limit is used, this number will typically be larger than the count, as it includes all items across all paginations, whether currently present or not.

### Usage

    $int = $paginatedArray->getTotal();

### Return value

`int`

Total number of items across all paginations.

