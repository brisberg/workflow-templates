# Create Release

This workflow simply responds to a new Tag being pushed, and create a corresponding GitHub Release. Using the official [actions/create-release](https://github.com/actions/create-release) Action.

Useful to reduce manual steps to perform a release (i.e. `yarn publish` will automatically create the tag).

The resulting release event can be used to trigger other workflows or third_party applications.

See the above action for more configuration options.

[Standard Workflow](https://github.com/brisberg/workflow-templates/blob/main/workflows/releases/create-release.yml)

## Improvements

Integrating some kind of tool which can generate release notes would be perfect for this workflow. So it can populate the `body` field.
