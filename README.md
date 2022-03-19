# PlatformOS Permission module

Creates the possibility to handle user roles and permission on your application.

## Usage

### Hooks

You can read more about `hooks` at [Hook module's](https://github.com/hosszukalman/pos-module-hook) page.

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
