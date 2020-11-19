# Create Release (with artifacts)

This workflow responds to a new Tag being pushed, and create a corresponding GitHub Release. Then build the project artifact using project specific steps, and uploads the final bundle to the release.

Using the official [actions/create-release](https://github.com/actions/create-release) Action and [actions/upload-release](https://github.com/actions/upload-release).

Useful to reduce manual steps to perform a release (i.e. `yarn publish` will automatically create the tag).

The resulting release event can be used third_party applications.

See the above action for more configuration options.

[Standard Workflow](https://github.com/brisberg/workflow-templates/blob/main/workflows/releases/upload-release.yml)

## Alternatives

See [experimental workflows](https://github.com/brisberg/workflow-templates/experimental/releases) for more ideas and variations.

## Improvements

Integrating some kind of tool which can generate release notes would be perfect for this workflow. So it can populate the `body` field.
