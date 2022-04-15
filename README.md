# Docker Build Tag Publish

This GitHub Action will build, tag, an publish your docker image.  The logic has been designed for our use case, but can be modifed for yours.

# Default Tagging Logic
The tagging logic works as follows:
1. If you have a value for `image_tag` then we will use that value.
2. If you set `sha` to `true` then we will tak with the SHA
3. If this is the default branch, then the tag will be `latest`
4. if this is a pull request, the the tag will be `pr-branch` where branch is the branch name.
5. Otherwise, we'll use the Tag or branch name.

### Inputs

The following can be used as `step.with` keys

| Name             | Type    | Description                        |
|------------------|---------|------------------------------------|
| `checkout` | T/F | Determines if we should chckout the repository.  Default is `true`, (optional) Set to `false` if this is being done in an eariler step |
| `image_tag` | string | overwrites default tagging logic with this tag, unless it is a Pull request.  (Optional) |
| `sha` | T/F | Set to `true` to use the SHA for the tag.  (Optional) |
| `org_name` | string | Docker org name.  (Optional) If not specified, assumes it to be the same as the GitHub Org Name |
| `repo_name` | string | The name of the Docker Repository.  (Optional) If not specified, will use the GitHub repo name. |

## Example 1

This will checkout the code, build, tag and push using the default tags

```yaml
-   uses: bitovi/github-actions-docker-publish@1.0.0
```

## License
The scripts and documentation in this project are released under the [MIT License](https://github.com/bitovi/github-actions-docker-publish/blob/main/LICENSE).

## Provided by Bitovi
[Bitovi](https://www.bitovi.com/) is a proud supporter of Open Source software.

## Customize
Please feel free to copy and customize this action for your specific use case.  Not sure where to start, Bitovi has consultants that can help.  Please contat us at contact@bitovi.com.
