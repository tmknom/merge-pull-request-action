# merge-pull-request-action

Merge a pull request.

<!-- actdocs start -->

## Description

This action merges a specified pull request.
If [auto-merge][auto-merge] is enabled for the repository,
the pull request will be merged automatically once all required reviews are approved and all status checks pass.

## Usage

```yaml
  steps:
    - name: Merge Pull Request
      uses: tmknom/merge-pull-request-action@v0
      with:
        pull-request: 10
```

## Inputs

| Name | Description | Default | Required |
| :--- | :---------- | :------ | :------: |
| pull-request | Specifies the pull request to merge as a `number`, `url`, or `branch`. | n/a | yes |

## Outputs

| Name | Description |
| :--- | :---------- |
| auto-merge | Indicates whether the auto-merge setting is enabled for the repository. |

<!-- actdocs end -->

## Permissions

| Scope         | Access |
| :------------ | :----- |
| contents      | write  |
| pull-requests | write  |

## FAQ

### What is auto-merge?

Auto-merge enables a pull request to merge automatically when all requirements are met.
These requirements include completing the necessary reviews and passing all required status checks.
With auto-merge, you don’t need to monitor the pull request manually, allowing you to focus on other tasks.

To use auto-merge, it must first be enabled for the repository.
Once enabled, users with write permissions can configure specific pull requests to merge automatically when all requirements are satisfied.

For more information, see:

- [Managing auto-merge for pull requests in your repository][releases]

### Can this action approve a pull request?

No.

This action does not approve pull requests.
If branch protection rules require approval, you must ensure the pull request is approved before using this action.

## Related projects

- [merge-workflows](https://github.com/tmknom/merge-workflows): Collection of merge workflows.

## Release notes

See [GitHub Releases][releases].

[auto-merge]: https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/configuring-pull-request-merges/managing-auto-merge-for-pull-requests-in-your-repository
[releases]: https://github.com/tmknom/merge-pull-request-action/releases
