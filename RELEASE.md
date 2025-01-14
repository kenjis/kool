# Release process

For generating a new release we follow the steps:

- Get latest `master` branch.
- Make sure docs are updated - `kool run make-docs`
- Make sure formatting is correct - `kool run fmt`
- Make sure there are no syntax/stylistic errors - `kool run lint`
- Make sure tests are passing - `kool run test`
- Pick the version name you wanna build - `export BUILD_VERSION=0.0.0` (taking into consideration [Semantic Versioning rules for Major, Minor and Patch versions](https://semver.org/#summary))
- Build all artifacts - `bash build_artifacts.sh`
- Review if documentation is updated accordingly (docs/)
- Upload to the existing draft release all the artifacts built at dist/ folder.
- Publish the new version (which will create the tag as well)
- In case of version bumping, check if we need to update `SECURITY.md` to show what version we currently support.
