Delete/clear the cache(s) identified by given name or wildcard
--------------------------------------------------------------

### Example

    // Delete cache named "my-cache-name"
    $cache->delete("my-cache-name");
    
    // Delete all caches starting with "my-"
    $cache->delete("my-*");

### Usage

    $bool = $cache->delete(string $name);

### Arguments

Name

Type(s)

Description

`name`

string

Name of cache, or partial name with wildcard (i.e. "MyCache\*") to clear multiple caches.

### Return value

`bool`

True on success, false if no cache was cleared

