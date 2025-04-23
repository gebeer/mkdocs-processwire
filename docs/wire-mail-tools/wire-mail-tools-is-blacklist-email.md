Is given email address in the blacklist?
----------------------------------------

*   Returns boolean false if not blacklisted, true if it is.
*   Uses `$config->wireMail['blacklist']` array unless given another blacklist array in $options.
*   Always independently verify that your blacklist rules are working before assuming they do.
*   Specify true for the `why` option if you want to return the matching rule when email is in blacklist.
*   Specify true for the `throw` option if you want a WireException thrown when email is blacklisted.

Available since version **3.0.129**.

### Example

    // Define blacklist in /site/config.php
    $config->wireMail('blacklist', [
      'email@domain.com', // blacklist this email address
      '@host.domain.com', // blacklist all emails ending with @host.domain.com
      '@domain.com', // blacklist all emails ending with @domain.com
      'domain.com', // blacklist any email address ending with domain.com (would include mydomain.com too).
      '.domain.com', // blacklist any email address at any host off domain.com (domain.com, my.domain.com, but NOT mydomain.com).
      '/something/', // blacklist any email containing "something". PCRE regex assumed when "/" is used as opening/closing delimiter.
      '/.+@really\.bad\.com$/', // another example of using a PCRE regular expression (blocks all "@really.bad.com").
    ]);
    
    // Test if email in blacklist
    $email = 'somebody@domain.com';
    $result = $mail->isBlacklistEmail($email, [ 'why' => true ]);
    if($result === false) {
      echo "<p>Email address is not blacklisted</p>";
    } else {
      echo "<p>Email is blacklisted by rule: $result</p>";
    }

### Usage

    // basic usage
    $bool = $mail->isBlacklistEmail(string $email);
    
    // usage with all arguments
    $bool = $mail->isBlacklistEmail(string $email, array $options = []);

### Arguments

Name

Type(s)

Description

`email`

string

Email to check

`options` (optional)

array

*   `blacklist` (array): Use this blacklist rather than [`$config->emailBlacklist`](/api/ref/config/email-blacklist/) (default=\[\])
*   `throw` (bool): Throw WireException if email is blacklisted? (default=false)
*   `why` (bool): Return string containing matching rule when email is blacklisted? (default=false)

### Return value

`bool` `string`

Returns true if email is blacklisted, false if not. Returns string if `why` option specified + email blacklisted.

### Exceptions

Method can throw exceptions on error:

*   **`WireException`** - if given a blacklist that is not an array, or if requested to via `throw` option.
    

