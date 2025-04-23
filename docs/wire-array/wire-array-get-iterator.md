Allows iteration of the WireArray.
----------------------------------

*   Fulfills PHP's IteratorAggregate interface so that you can traverse the WireArray.
*   No need to call this method directly, just use PHP's `foreach()` method on the WireArray.

### Example

    // Traversing a WireArray with foreach:
    foreach($items as $item) {
      // ...
    }

### Usage

    $arrayObject = $wireArray->getIterator();

### Return value

`ArrayObject` [`Wire`](/api/ref/wire/)

\[\]

