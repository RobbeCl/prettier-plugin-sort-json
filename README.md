# prettier-plugin-sort-json

A plugin for [Prettier](https://prettier.io) that sorts JSON files by property name.

## Requirements

This module requires an [LTS](https://github.com/nodejs/Release) Node version (v10.0.0+), and `prettier` v2.1.0+.

## Install

Using `npm`:

```console
npm install --save-dev prettier-plugin-sort-json-custom
```

Using `yarn`:

```console
yarn add --dev prettier-plugin-sort-json-custom
```

## Description

This plugin adds a JSON preprocessor that will sort JSON files containing a JSON object alphanumerically by key. JSON files containing Arrays or other non-Object values are skipped.

Object entries are sorted by key using [`Array.sort`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort), according to each character's Unicode code point value.

## Examples

Before:

```json
{
    "z": null,
    "a": null,
    "b": null,
    "0": null,
    "exampleNestedObject": {
        "z": null,
        "a": null
    }
}
```

After:

```json
{
    "0": null,
    "a": null,
    "b": null,
    "exampleNestedObject": {
        "z": null,
        "a": null
    },
    "z": null
}
```

## Configuration

### JSON Recursive Sort

Sort JSON objects recursively, including all nested objects.

| Default | CLI Override            | API Override                |
| ------- | ----------------------- | --------------------------- |
| `false` | `--json-recursive-sort` | `jsonRecursiveSort: <bool>` |

# Remarks:

This code is official from https://github.com/Gudahtt/prettier-plugin-sort-json with a pull request from https://github.com/MasterEric/prettier-plugin-sort-json which was never approved. So I created this custom project which is published to npm to people can actually use it.
