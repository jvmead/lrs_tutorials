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


TOPICS TO DEVELOP FURTHER:
- accessing information already in flow (once demonstrated interactively... integral, fprompt, ToT_1,2)
- pathway to waveform noise filtering and optionally the SPE response deconvolution [https://github.com/DUNE/ndlar_flow/blob/develop/src/proto_nd_flow/reco/light/wvfm_noise_filter.py, https://github.com/DUNE/ndlar_flow/blob/develop/src/proto_nd_flow/reco/light/wvfm_deconv.py]
- pathway to clustering / flash building [https://github.com/DUNE/ndlar_flow/blob/develop/src/proto_nd_flow/reco/light/flash_finder.py]
- pathway to spatial reconstruction [https://github.com/jvmead/light_file_processing, https://github.com/jvmead/lrs_spatial_reco]
- trigger thresholding exploration [https://github.com/jvmead/light_file_processing]
- employing interaction/segment timestamps for 'true hit/flash' defintion [https://github.com/jvmead/light_file_processing]
- using truth backtracking