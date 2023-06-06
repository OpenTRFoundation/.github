Common GitHub settings for all repos in the org. The configuration files for each of our GitHub Apps are in the `.github/` folder.

`settings.yml`: This configures the settings for your GitHub repository. The settings are applied by the ["Settings" GitHub App](https://probot.github.io/apps/settings).

[`probot-config`](https://github.com/probot/probot-config) extension is used to share `settings.yml`. This way changes in this repo will be  automatically extend to all other repositories.

To load the shared settings in your repository, create a `.github/settings.yml` file with the following content:

```yaml
_extends: .github
```

Then overwrite any settings you want to change (deepmerge is used).

```yaml
_extends: .github

repository:
  has_wiki: true
  has_projects: true
  ...
```
TEST
