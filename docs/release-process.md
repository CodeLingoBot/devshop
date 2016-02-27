Release Process
===============

There's a lot of moving parts so creating a new release is not simple.

Follow this guide.

1. Create new releases for contrib projects, if necessary.
  - hosting_solr
  - hosting_logs
  - etc
4. Update `opendevshop/devmaster/devmaster.make` with the latest version of drupal core.
3. Update `opendevshop/devmaster/devmaster.make` with the latest releases of contrib modules.
4. Update `opendevshop/devshop/vars.yml` with the latest versions of drush modules.
5. Using the commit log as your guide, add a list of new features to the CHANGELOG.org in the devshop repo.  Use the "x commits since this release" feature on github's releases page.  Include changes in both devshop and devmaster repos in the changelog.
7. Update `opendevshop/devshop/docs/install.md` with the latest version in the example install script.
2. Create a new release branches for devmaster, devshop, and devshop_provision repos using the `release-prep.sh` script. This script takes a version for an argument and creates release branches in the three repos.
6. In your release branch, edit the version in the files:
  - `build-devmaster.make`
  - `install.sh`
  - `vars.yml`
  - `opendevshop/devmaster/VERSION.txt` 
5. Create and push a new tag for `devmaster`, `devshop`, and `devshop_provision` using the `release.sh` script.  This script takes a version for an argument and creates release tags in the three repos.
6. Create a new "release" on github to match the new tag at https://github.com/opendevshop/devshop/releases/new.  Copy the release notes from CHANGELOG.md into 
7. Edit http://drupal.org/project/devshop to show the latest release.
8. Update the "Current Version" displayed on the gh-pages branch. https://github.com/opendevshop/devshop/edit/gh-pages/index.html 
7. Announce!