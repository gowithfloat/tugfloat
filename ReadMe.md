tugfloat
========
Manage [Tugboat](https://www.tugboatqa.com) previews by git branch name. This is primarily useful if you are using a custom CI/CD (i.e. Jenkins) with Tugboat.

Requirements
------------
* Tugboat CLI - https://docs.tugboatqa.com/tugboat-cli/
* jq - https://stedolan.github.io/jq/

Environment Variables
-----
* `TUGBOAT_TOKEN` - your Tugboat token (https://dashboard.tugboatqa.com/access-tokens)
* `TUGBOAT_REPO_ID` - the ID number for the repo (you can find this in the URL)

Examples
-----
### Launch/update new preview for `feature/my-feature`
tugfloat -o launch -b feature/my-feature

### Launch/update a new preview for `feature/my-feature` based on a base preview
tugfloat -o launch -b feature/my-feature -p main

### Retrieve the URL to a preview for `feature/my-feature`
tugfloat -o link -b feature/my-feature

### Retrieve the ID of a preview for `feature/my-feature`
tugfloat -o id -b feature/my-feature

### Delete a preview for `feature/my-feature`
tugfloat -o sink -b feature/my-feature