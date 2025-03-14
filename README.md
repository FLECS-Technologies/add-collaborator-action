# FLECS Add Collaborator Action
A GitHub action to add a collaborator to a repository

# Usage
## Example
```yml
uses: FLECS-Technologies/add-collaborator-action@v1.x
with:
  repo: "repository-name"
  owner: "organization"
  username: "user1"
  permission: "maintain"
env:
  GITHUB_TOKEN: "access token with with repo admin permission"
```

# Inputs
| Name               | Description                                  | Example              | Required | Default |
| ------------------ | -------------------------------------------- | -------------------- | -------- | ------- |
| repo               | Name of the repository                       | "awesome-project"    | Yes      | -       |
| owner              | Repository owner                             | "FLECS-Technologies" | Yes      | -       |
| usernames          | GitHub user to add as collaborator           | "user1"              | Yes      | -       |
| permission         | one of (pull\|triage\|push\|maintain\|admin) | "maintain"           | No       | "push"  |

See [GitHub REST API documentation]([https://docs.github.com/en/rest/repos/repos?apiVersion=2022-11-28#create-an-organization-repository](https://docs.github.com/en/rest/collaborator/collaborator?apiVersion=2022-11-28#add-a-repository-collaborator)) for further examples and explanation.

# Environment
| Name          | Description                                                                                                       | Required |
| ------------- | ----------------------------------------------------------------------------------------------------------------- | ---------|
| GITHUB\_TOKEN | A GitHub access token or GitHub Apps installastion token with the "Administration" repository permissions (write) | true     |

# License
[Apache 2.0](https://github.com/FLECS-Technologies/add-collaborator-action/blob/v1.x/LICENSE)
