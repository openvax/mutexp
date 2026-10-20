# Releasing

After the version bump PR passes CI and merges, release from a clean `master`
checkout with Python 3.11 or newer:

1. Verify the version in `mutexp/__init__.py` is absent from PyPI.
2. Install `build` and `twine`, then run `python -m build` and
   `python -m twine check --strict dist/*`.
3. Upload with `python -m twine upload dist/*`.
4. Tag the merge commit as `v<version>` and push the tag.

Check the version-specific PyPI page and its `Requires-Python` metadata before
closing the release task.
