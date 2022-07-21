# Event Based Release Workflows

This set of workflows is meant to work together as the `upload-artifact` workflow is keyed off the release event from the `create-release` workflow.

The purpose here is to divide the concerns about Generating the Release and potentially Release Notes from the aspects of actually building the project.

In the case where the release notes generator is written in python and the project is build in go, each workflow will be substantially simpler than interleaved.

## Important

This doesn't actually work without a PAT. By default Github workflows cannot initiate other workflows if they use the built in GITHUB_TOKEN.
