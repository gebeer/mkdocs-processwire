Get the value of a MySQL variable
---------------------------------

### Example

    // Get the minimum fulltext index word length
    $value = $database->getVariable('ft_min_word_len');
    echo $value; // outputs "4"

### Usage

    // basic usage
    $string = $database->getVariable(string $name);
    
    // usage with all arguments
    $string = $database->getVariable(string $name, bool $cache = true, bool $sub = true);

### Arguments

Name

Type(s)

Description

`name`

string

Name of MySQL variable you want to retrieve

`cache` (optional)

bool

Allow use of cached values? (default=true)

`sub` (optional)

bool

Allow substitution of MyISAM variable names to InnoDB equivalents when InnoDB is engine? (default=true)

### Return value

`string` `null`

