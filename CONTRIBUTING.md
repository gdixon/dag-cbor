
# Contributing

All contributions, big and small, are very appreciated!
[File an issue](#file-an-issue) for bug reports, suggestions and questions, or [make a pull request](#make-a-pull-request) to actively contribute to the code or documentation.

However you decide to help, please refer to our [code of conduct](CODE_OF_CONDUCT.md) for what we expect from our community.


## File an Issue

Issues can be filed at https://github.com/hashberg-io/dag-cbor/issues. You can file an issue to:

- report a bug (using the `bug` label)
- suggest a new feature (using the `enhancement` label)
- suggest improvements to our documentation (using the `documentation` label)
- ask for information and start a discussion thread (using the `question` label)

If you are reporting a bug, please include the following information:

- project version (PyPI version number or commit number)
- Python version
- version of installed dependencies
- how the bug manifests (e.g. what you expect to happen vs what actually happens)
- how others can reproduce the bug

Please try to be concise in your description, providing a minimal reproducible example whenever possible.

If you're proposing a new feature, please describe it in detail, with a few examples of it might be implemented and of its intended usage.


## Make a Pull Request

You can [make a pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) to:

- fix a bug which is reported and discussed in an open issue
- implement a new feature which is suggested and discussed in an open issue
- improve our documentation in ways suggested and discussed in an open issue

You should [link your pull request to the issue(s)](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue) that it addresses. Once your pull request passes all continuous integration checks, we will review it and either:

- approve the pull request and merge it
- start a discussion on how to improve the pull request before it can be approved
- reject the pull request, with an explanation as to why we don't consider it viable for improvement


### Continuous Integration

You can perform continuous integration checks on all supported versions by running [tox](https://tox.readthedocs.io/en/latest/) in the main project folder:

```
tox
```

Continuous integration involves the following individual checks:

1. testing with [pytest](https://docs.pytest.org/):

```
pytest test
```

2. static type-checking with [mypy](http://mypy-lang.org/):

```
mypy dag-cbor
```

3. linting with [pylint](https://www.pylint.org/):

```
pylint dag-cbor
```

Whenever relevant, please consider contributing some additional tests pertaining to your implementation.


### Documentation

The API documentation for this project is generated automatically by [pdoc](https://pdoc3.github.io/pdoc/):

```
pdoc --config latex_math=True --config show_type_annotations=True --force --html --output-dir docs dag-cbor
```

If you write new functions, classes or modules, please consider documenting them using Markdown docstrings, in pdoc's format.

If you edit the [readme page](README.md), please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.
