# DJsonSchema
[JSON Schema](http://json-schema.org/) draft v4 reader and code generator for Delphi.

## Features

- command line tool for generation of boilerplate code to read JSON documents
- generated code can be adjusted via [Mustache](https://mustache.github.io/) templates
- JSON Schema draft v4 is only partially supported

## Usage

```
djsonsgen.exe <json_schema> <template_dir> [options]

<json_schema>                    - JSON Schema file
<template_dir>                   - Template source directory
[-o<path>], [/output_dir:<path>] - Output directory (default = use json_schema
                                   filename as directory)
```

**Example:** `djsonsgen.exe draft-04-schema.json .\templates`

- [Writing templates for DJsonSchema](/src/templates/README.md)

## Compilation/Contribution

These are the steps if you want to compile the project for your own purposes or if you like to contribute to this project.

### Get the code

`git clone --recursive https://github.com/schlothauer-wauer/DJsonSchema.git`

The `recursive` parameter is **required** to clone/update also the *submodule* `src/dmustache` (SynMustache). Alternatively you could run the following commands:

```
git clone https://github.com/schlothauer-wauer/DJsonSchema.git
cd DJsonSchema
git submodule update --init --recursive
```

[SynMustache](https://github.com/synopse/dmustache) is used as *Mustache* template engine.

### Delphi

**DJsonSchema** is originally written with *Delphi 10.1* (no idea what the minimum required version is). :blush:
