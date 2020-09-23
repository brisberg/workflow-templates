# Yarn (Build, Test, Lint) in sub jobs

Attempting to reconfigure [yarn-build-test-lint](https://github.com/brisberg/workflow-templates/blob/main/workflows/yarn-build-test-lint.md) workflow into a series of jobs.

The advantage is that in the Actions UI it will split out the results of each step, making it clear at a glance what failed. Also it will still run `lint` and `test` when the other fails which is desirable to fix mistakes in less CI runs.

This version uses `actions/upload-artifact` to pass the built files between jobs. Currently this isn't actually necessary, but it would be useful to release scripts. The main issue is the large amount of duplication between each job. They are all nearly identical except the last step.

[Workflow](https://github.com/brisberg/workflow-templates/blob/main/experimental/yarn-build-test-lint-jobs.yml)
