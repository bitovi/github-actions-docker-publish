# Docker Build Tag Publish

This GitHub Action will build, tag, an publish your docker image.  The logic has been designed for our use case, but can be modifed for yours.

# CI Tagging

### Inputs

The following can be used as `step.with` keys

| Name             | Type    | Description                        |
|------------------|---------|------------------------------------|
| `checkout` | boolean | Determines if we should chckout the repository.  Default is true, (optional) |
| `dLatest` | boolean | Tag the default branch with latest instead of branch name.  Default is true (optional |)
| `name` | string | Name of the image, minus the repository. Default is the GitHub Reponame. (Optional) |

## Example usage

```yaml
-   uses: bitovi/github-actions-docker-publish@1.0.0
    with:
        checkout: false



```

## License
The scripts and documentation in this project are released under the [MIT License](https://github.com/bitovi/github-actions-docker-publish/blob/main/LICENSE).

## Provided by Bitovi
[Bitovi](https://www.bitovi.com/) is a proud supporter of Open Source software.

## Customize
Please feel free to copy and customize this action for your specific use case.  Not sure where to start, Bitovi has consultants that can help.  Please contat us at contact@bitovi.com.
