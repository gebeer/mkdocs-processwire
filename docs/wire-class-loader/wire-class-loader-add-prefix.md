Map a class prefix to a path
----------------------------

This is used as a helper/fallback and class is not required to be in given path, but the path will be added as another to check when not found in namespace path(s).

### Usage

    $classLoader->addPrefix(string $prefix, string $path);

### Arguments

Name

Type(s)

Description

`prefix`

string

Case sensitive prefix specific to class name (not namespace).

`path`

string

