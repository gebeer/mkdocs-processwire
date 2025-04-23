Add a namespace to point to a path root
---------------------------------------

Multiple root paths may be specified for a single namespace by calling this method more than once.

### Example

    $classLoader->addNamespace('HelloWorld', '/path/to/that/');

### Usage

    $classLoader->addNamespace(string $namespace, string $path);

### Arguments

Name

Type(s)

Description

`namespace`

string

`path`

string

Full system path

