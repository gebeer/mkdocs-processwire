Quickly set field value(s) and save to database
-----------------------------------------------

You can specify a single field and value, or an array of fields and values.

This method does not need output formatting to be turned off first, so make sure that whatever value(s) you set are not formatted values.

### Examples

    // Set and save the summary field
    $page->setAndSave('summary', 'When nothing is done, nothing is left undone.');

    // Set and save multiple fields
    $page->setAndSave([
      'title' => 'It is Friday again',
      'subtitle' => 'Here is another new blog post',
      'body' => 'Hope you all have a great weekend!'
    ]);

    // Update a 'last_login' field after every user login
    $session->addHookAfter('loginSuccess', function($event) {
      $user = $event->arguments(0);
      $user->setAndSave('last_login', time());
    });

### Usage

    // basic usage
    $bool = $page->setAndSave($key);
    
    // usage with all arguments
    $bool = $page->setAndSave($key, $value = null, array $options = []);

### Arguments

Name

Type(s)

Description

`key`

array, string

Field or property name to set, or array of one or more \['property' => $value\].

`value` (optional)

string, int, bool, object

Value to set, or omit if you provided an array in first argument.

`options` (optional)

array

See Pages::save() for additional $options that may be specified.

### Return value

`bool`

Returns true on success, false on failure

### See Also

*   [Blog post about setAndSave](https://processwire.com/blog/posts/processwire-2.6.9-core-updates-and-new-procache-version/)
*   [Pages::save()](/api/ref/pages/save/)

