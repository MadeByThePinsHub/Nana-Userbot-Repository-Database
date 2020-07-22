# Nana Userbot Repository Database

This repository contains the database files needed for the Nana Userbot Updater feature to work
and to allow pajeets to switch between repositories.

## Schema

This is how the schema of the `config/repo.json` file looks like. If you want to have your own fork of Nana
to be added in the database, consider reading the schema documentation below. Here's what it looks like.

```json
{
  "Nana-Userbot-New" : {
    "Author" : "Pokurt",
    "repo-link" : "https://github.com/pokurt/Nana-Remix",
    "version" : {
      "latest" : {
        "is-beta" : false,
        "dockerfile" : "https://raw.githubusercontent.com/pokurt/Nana-Remix/master/Dockerfile",
        "description" : "Official version of Nana userbot, maintained by Pokurt."
      }
    }
  }
}
```

### `Nana-Userbot-New`

Slug of the Nana Userbot repository for easy identification.

#### `Author`

An string of the author of the Nana userbot, preferrly GitHub/GitLab username.

#### `repo-link`

Link to an GitHub or GitLab repository of their Nana userbot.

#### `version`

Each version should have `is-beta`, `dockerfile` and `description` fields filled up. We'll detail it a little bit below.

In each version, whenever its `latest` (or `stable`) or `develop`, each must have the following:
* `is-beta`: Boolean, defaults to `false` if its stable release.
* `dockerfile`: Link to raw Dockerfile, like `https://raw.githubusercontent.com/pokurt/Nana-Remix/master/Dockerfile`.
* `description`: An nice description about that version.
