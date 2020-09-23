# Yarn (Build, Test, Lint)

Most Javascript/Typescript packages or applications will use Npm or Yarn as their package manager. I have chosen to standardize my own repositories on Yarn.

Generally, repositories will want to run their specified `build`, `test`, and `lint` scripts through the package manager to verify the correctness of new changes. This workflow makes it simple to run these commands in a GitHub Actions Workflow.

## Features

#### Matrix Strategy

The workflow uses a Matrix Strategy declaration which makes it simple to run multiple workflows in parallel for different Node.js versions.

#### Dependency Caching

The workflow uses GitHub's standard [actions/cache](https://github.com/actions/cache) action to cache the downloaded yarn dependencies. It is based on their standard [example](https://github.com/actions/cache/blob/master/examples.md#node---yarn) config.

This works by hashing the `yarn.lock` file to generate a cache key. This means that caching will get more hits if you do not update yarn dependencies very often.

## Improvements

I would like to improve this workflow into more modular jobs. That way you get more easily distinguished output in the Actions Tab.

[Standard Workflow](https://github.com/brisberg/workflow-templates/workflows/yarn-build-test-lint.yml)
