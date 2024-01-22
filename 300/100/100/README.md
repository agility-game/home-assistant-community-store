# 100 - Connect with Personal Access Token

Personal access tokens can only be used to connect GitHub.com repositories to GitLab, and the GitHub user must have the [owner role](https://docs.github.com/en/get-started/learning-about-github/access-permissions-on-github).

To perform a one-off authorization with GitHub to grant GitLab access your repositories:

1. In GitHub, create a token:
   - a. Open https://github.com/settings/tokens/new
   - b. Create a **Personal Access Token**
   - c. Enter a **Token description** and update the scope to allow ```repo``` and ```admin:repo_hook``` so that GitLab can access your project, update commit statuses, and create a web hook to notify GitLab of new commits.

2. In GitLab, create a project:
   - a. On the left sidebar, at the top, select **Create new (+)** and **New project/repository**.
   - b. Select **Run CICD for external repository**.
   - c. Select **GitHub**.
   - d. For **Personal Access Token**, paste the token.
   - e. Select **List Repositories**.
   - f. Select **Connect** to select the repository.

4. In GitHub, add ```.gitlab-ci.yml``` to [configure GitLab CI/CD](https://docs.gitlab.com/ee/ci/quick_start/index.html).

GitLab:

1. Imports the project (here: ...).
2. Enables [Pull Mirroring](https://docs.gitlab.com/ee/user/project/repository/mirror/pull.html).
3. Enables [GitHub project integration](https://docs.gitlab.com/ee/user/project/integrations/github.html).
4. Create a web hook on GitHub to notify GitLab of new commits.
