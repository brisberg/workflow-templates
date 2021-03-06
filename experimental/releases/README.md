# Release Management

GitHub offers [official actions](https://github.com/actions) for interacting with parts of the GitHub API. Some of these are specifically around creating "Releases" on the GitHub platform.

A ["Release"](https://docs.github.com/en/free-pro-team@latest/github/administering-a-repository/about-releases) in GitHub terminology is a block of metadata defining a package of your software for others to use. This can include a Name, Release Notes, Binary Artifacts, etc.

It is useful as releases are displayed on the project home page.

If users will not be pulling your artifacts from GitHub itself (say though NPM instead), it is necessary to publish your package there as well. However, you can key workflows to publish to other registries off the ["release event"](https://developer.github.com/webhooks/event-payloads/#release) generated by the workflow.

This directory includes some flavors of for creating and modifying releases.
