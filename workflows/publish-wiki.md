# Publish Wiki

All GitHub repositories can be equipped with a Wiki repository, also hosted by GitHub. Internally, this Wiki is actually a separate Git repository (located at `github.com/username/repo.wiki.git`).

Coordinating changes between these two repositories can be a challenge. The cleanest solution I have found is to move the Wiki into the main repo, treat the real Wiki repo as Read-Only (no edits through the UI), and use a GitHub Action to sync changes from `main` to the Wiki repo.

This can be easily accomplished using [GitHub-Wiki-Action](https://github.com/Andrew-Chen-Wang/github-wiki-action) with minimal setup.

See the above action for more configuration options.

[Standard Workflow](https://github.com/brisberg/workflow-templates/blob/main/workflows/publish-wiki.yml)
