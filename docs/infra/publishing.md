# Publishing wave-lang packages to PyPI

1. Before publishing, consider triggering the "Build and release packages"
workflow to build Python wheels from the latest commit on `main`. This workflow
is also automatically triggered every night. Note that the package is not tested
after it is built (nor before publishing), so make sure the latest commit passes
all tests.

2. Manually trigger the "Publish to PyPI" workflow, which uses
[Trusted Publishing](https://docs.pypi.org/trusted-publishers/). You will need
the run ID of the specific "Build and release packages" workflow whose Python
wheels you want to publish.
