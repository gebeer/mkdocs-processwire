Format a date, using PHP date(), strftime() or other special strings (see arguments).
-------------------------------------------------------------------------------------

This is designed to work the same way as PHP's `date()` but be able to accept any common format used in ProcessWire. This is helpful for reducing code in places where you might have logic determining when to use `date()`, `strftime()`, `wireRelativeTimeStr()` or some other date formatting function.

### Example

    // Output the current date/time in relative format
    echo $datetime->date('relative');

### Usage

    // basic usage
    $string = $datetime->date();
    
    // usage with all arguments
    $string = $datetime->date($format = '', $ts = null);

### Arguments

Name

Type(s)

Description

`format` (optional)

string, int

Use one of the following:

*   [PHP date](http://php.net/manual/en/function.date.php) format
*   [PHP strftime](http://php.net/manual/en/function.strftime.php) format (detected by presence of a '%' somewhere in it)
*   `relative` for a relative date/time string.
*   `relative-` for a relative date/time string with no tense.
*   `rel` for an abbreviated relative date/time string.
*   `rel-` for an abbreviated relative date/time string with no tense.
*   `r` for an extra-abbreviated relative date/time string.
*   `r-` for an extra-abbreviated relative date/time string with no tense.
*   `ts` makes it return a unix timestamp
*   blank string makes it use the system date format ($config->dateFormat)
*   If given an integer and no second argument specified, it is assumed to be the second ($ts) argument.

`ts` (optional)

int, string, null

Optionally specify the date/time stamp or strtotime() compatible string. If not specified, current time is used.

### Return value

`string` `bool`

Formatted date/time, or boolean false on failure

