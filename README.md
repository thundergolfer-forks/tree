# Tree

`tree` is a library for working with nested data structures. In a way, `tree`
generalizes the builtin `map` function which only supports flat sequences,
and allows to apply a function to each "leaf" preserving the overall
structure.

```python
>>> import tree
>>> structure = [[1], [[[2, 3]]], [4]]
>>> tree.flatten(structure)
[1, 2, 3, 4]
>>> tree.map_structure(lambda v: v**2, structure)
[[1], [[[4, 9]]], [16]]
```

`tree` is backed by an optimized C++ implementation suitable for use in
demanding applications, such as machine learning models.

## Installation

Install `tree` by running:

```shell
$ pip install dm-tree
```

## Support

If you are having issues, please let us know by filing an issue on our
[issue tracker](https://github.com/deepmind/tree/issues).

## Development

Install Bazel using `bazel/install.sh` or by some other method.

## License

The project is licensed under the Apache 2.0 license.
