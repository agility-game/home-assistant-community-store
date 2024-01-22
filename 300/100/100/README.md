# 100 - Connect with Personal Access Token

Personal access tokens can only be used to connect GitHub.com repositories to GitLab, and the GitHub user must have the [owner role](https://docs.github.com/en/get-started/learning-about-github/access-permissions-on-github).

To perform a one-off authorization with GitHub to grant GitLab access your repositories:

1. In GitHub, create a token:
   - a. Open https://github.com/settings/tokens/new
   - b. Create a **Personal Access Token - Fine-grained tokens** (In *Beta* at the time of this writing)
   - c. Enter a **Token Name** (here: ```Agility-Game-HACS-PAT```) and a **Token description** (here: ```Agility Game - Home Assistant Community Store (HACS) - Personal Access Token```), choose an **Expiration** (here: 90 days), with a **Resource owner** (here: ```agility-game```). For Repository Access choose **Only select repositories** and choose the repository (here: ```agility-game/home-assistant-community-store```). For Permissions, for Repository permissions, **allow read and write** for ```Actions```, ```Content```, ```Issues```, ```Webhooks``` and ```Workflows``` so that GitLab can access your project, update commit statuses, and create a web hook to notify GitLab of new commits. Finally, click **Generate token** and copy the token to a safe location for further processing.

2. In GitLab, create a project within ```https://gitlab.com/agility-game/home-assistant/```:
   - a. Select **Create new project**.
   - b. Select **Run CICD for external repository**.
   - c. Select **GitHub**.
   - d. For **Personal Access Token**, paste the token (here: the token named ```Agility-Game-HACS-PAT``` we saved earlier) and click **Authenticate**.
   - e. Select **Collaborated** tab and choose to **import** the GitHub repository (here: ```agility-game/home-assistant-community-store```). If ```agility-game/home-assistant-community-store``` it is not listed, make sure you add yourself as a Collaborator to the GitHub repository (here: ```agility-game/home-assistant-community-store```) via **Settings** > **Collaborators and teams** for this GitHub repository.
   - f. Under **Advanced import settings**, do **not** check ```Import collaborators```, as this will consume seats on your GitLab instance.
   - g. For **To GitLab** pick **agility-game/home-assistant** / **home-assistant-community-store**.
   - h. Select **Connect** to select the repository (here: ```agility-game/home-assistant-community-store```).

4. In GitHub, add ```.gitlab-ci.yml``` to [configure GitLab CI/CD](https://docs.gitlab.com/ee/ci/quick_start/index.html).

GitLab:

1. Imports the project (here: ```agility-game/home-assistant-community-store```).
2. Enables [Pull Mirroring](https://docs.gitlab.com/ee/user/project/repository/mirror/pull.html).
3. Enables [GitHub project integration](https://docs.gitlab.com/ee/user/project/integrations/github.html).
4. Create a web hook on GitHub to notify GitLab of new commits.
