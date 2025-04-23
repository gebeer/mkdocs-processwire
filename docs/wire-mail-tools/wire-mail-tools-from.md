Return new WireMail instance populated with “from” email
--------------------------------------------------------

Available since version **3.0.113**.

### Usage

    // basic usage
    $wireMail = $mail->from(string $email);
    
    // usage with all arguments
    $wireMail = $mail->from(string $email, $name = null);

### Arguments

Name

Type(s)

Description

`email`

string

Must be a single email address or "User Name <user

`name` (optional)

### Return value

[`WireMail`](/api/ref/wire-mail/)

