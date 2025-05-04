### Readme
Uses bump-my-project to bump version of the package automatically.

Config for both the package building and version bumping is in pyproject.toml.
Config for the build is under "[project]" and for bump-my-version under "[tool.bumpversion]".

### Release Workflow

When a new version tag is pushed:
    
    if new_version != prev_version:
        trigger bump-my-version to match the version in the tag;
        commit version change;
        push the version tag again to associate the commit with the updated package version (from last step) to the tag.
