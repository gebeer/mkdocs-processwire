Send the email
--------------

Call this method only after you have specified at least the `subject`, `to` and `body`.

### Usage

    $int = $m->send();

### Return value

`int`

Returns a positive number (indicating number of addresses emailed) or 0 on failure.

