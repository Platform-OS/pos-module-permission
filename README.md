# PlatformOS Permission module

Creates a thin access control layer that can be used by other (for example the user) modules. `can_do` and `can_do_or_unauthorized` will receive a requester entity that must have a permissions array, so requester is something similar like a requester interface that must be an implementation to get the entity's permissions.

## Installation

The currently suggested approach is to use git submodules. It will be replaced with a pOS module manager in the feature. For now, ensure the `modules` directory exists in your root directory and add a git submodule:

`git submodule add --name permission git@github.com:Platform-OS/pos-module-permission.git modules/permission`

To update your modules to the newest version, use `git submodule update --recursive --remote`

## Usage

### Hooks

You can read more about `hooks` at [Core module's](https://github.com/hosszukalman/pos-module-core) page.

#### `permission`

You can define your custom permissions by creating `hook_permission.liquid` in you application. For example:

```
{% comment %}
  Implements hook_permission.
{% endcomment %}
{% liquid
  assign permissions = '["permissions.manage"]' | parse_json
  return permissions
%}
```
## Versioning

```
git fetch origin --tags
npm version major | minor | patch
```
