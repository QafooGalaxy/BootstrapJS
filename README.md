# BootstrapJS

## Description

Install an JavaScript project bootstrap from one of the [BootstrapJS]()
Repositories.

## Usage

```yaml
- role: BootstrapJS
  flavor: "browser-requirejs-vanilla"
```

## Configuration

*optional* `user`: User the destination should belong to. (Default: `{{
ansible_env.USER }}`).

*optional* `homedir`: Homedir of the user the destination belongs to. It will
be used to calculate the default `destination` (Default: `{{ ansible_env.HOME
}}`).

*optional* `destination`: Target to install the BootstrapJS environment to.
(Default: `{{ homedir }}/BootstrapJS/{{ flavor }}`).

## Implicit Dependencies

- Git

## Further Remarks

In order to fully initialize the BootstrapJS Environment you need to run `npm
install && bower install && grunt symlink`. Therefore a running NodeJs
environment is required for full initialization. The [nvm]() role may help you
with that. The [npm]() role can help you with the corresponding initialization,
if you like.
