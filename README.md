make a directory in your user area called `dune` and containing a clone of this repo.
it should also contain a clone of these repositories:
- https://github.com/jvmead/lrs_sanity_check
- https://github.com/jvmead/ndlar-flow
The former is for accessing csv versions of geometry/calib/status information found in other formats in other repos.
The latter is for using the python environment from ndlar-flow as the starting point for the one I use for these tutorials.

You should be able to check what's included using something like:
```
import pkg_resources
import sys
sorted(
    [(d.project_name, d.version) for d in pkg_resources.working_set],
    key=lambda x: x[0].lower()
)
```
Or simply run with ndlar-flow's env and `pip install ...` whatever you don't have.