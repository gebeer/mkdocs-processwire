Send an email, drop-in replacement for PHP mail() that uses the same arguments
------------------------------------------------------------------------------

This is an alternative to using the [`$mail->send()`](/api/ref/mail/send/) method, and may be simpler for those converting existing PHP `mail()` calls to WireMail calls.

This function duplicates the same arguments as PHP’s mail function, enabling you to replace an existing PHP `mail(…)` call with [`$mail->mail(…)`](/api/ref/mail/mail/).

But unlike PHP’s mail function, this one can also send HTML (or multipart) emails if you provide an `$options` array for the `$message` argument (rather than a string). See the options array for the [`$mail->send()`](/api/ref/mail/send/) method for details.

### Example

    // 1. Basic PHP mail() style usage
    $mail->mail('ryan@processwire.com', 'Subject', 'Message body');
    
    // 2. PHP mail() style usage with with $headers argument
    $mail->mail('ryan@processwire.com', 'Subject', 'Message body', 'From: hello@world.com');
    
    // 3. Alternate usage with html and text body
    $mail->mail('ryan@processwire.com', 'Subject', [
      'bodyHTML' => '<html><body><h1>Message HTML body</h1></body</html>',
      'body' => 'Message text body',
      'from' => 'hello@world.com',
    ]);

### Usage

    // basic usage
    $bool = $mail->mail($to, string $subject, $message);
    
    // usage with all arguments
    $bool = $mail->mail($to, string $subject, $message, array $headers = []);

### Arguments

Name

Type(s)

Description

`to`

string, array

Email address TO. For multiple, specify CSV string or array.

`subject`

string

Email subject

`message`

string, array

Email body (PHP mail style), OR specify $options array with any of the following:

*   `bodyHTML` (string): Email body (HTML)
*   `body` (string): Email body (text). If not specified, and bodyHTML is, then text body will be auto-generated.
*   `from` (string): From email address
*   `replyTo` (string): Reply-to email address
*   `headers` (array): Associative array of header name => header value

`headers` (optional)

array

Optional additional headers as \[name=value\] array or "Name: Value" newline-separated string. Use this argument to duplicate PHP mail() style arguments. No need to use if you used $options array for the $message argument.

### Return value

`bool`

True on success, false on fail.

