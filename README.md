# setup-commandbox

Sets up [CommandBox CLI](https://www.ortussolutions.com/products/commandbox) for GitHub Actions.

## Inputs

The following are all the different input variables you can use on the action so you can setup CommandBox with ForgeBox API keys, default packages, specific versions and much more.

| Input                    | Type          | Default       | Description |
| -------------            | ------------- | ------------- | ----------- |
| `forgeboxAPIKey`         | string        | ---           | If added to the action, we will seed it in CommandBox for you.
| `installSystemModules`   | boolean       | `false`       | If true then it will install: `commandbox-cfconfig, commandbox-dotenv` for you
| `install`                | string        | ---           | If added, a comma-delmitted list of packages to install upon installation of the binary for you.
| `warmup`                 | boolean       | `false`       | If true and no install inputs detected, it will run the box binary.
| `version`                | semver        | `latest`      | The CommandBox version to install, if not passed we use the latest stable.

## Usage

Simple usage:

```yaml
- name: Setup CommandBox
  uses: Ortus-Solutions/setup-commandbox@v2.0.1
```

With Global Dependencies:

```yaml
- name: Setup CommandBox
  uses: Ortus-Solutions/setup-commandbox@v2.0.1
  with:
    installSystemModules: true
```

With Specific Dependencies:

```yaml
- name: Setup CommandBox
  uses: Ortus-Solutions/setup-commandbox@v2.0.1
  with:
    install: commandbox-fusionreactor
```

With ForgeBox Token

```yaml
- name: Setup CommandBox With ForgeBox Key
  uses: Ortus-Solutions/setup-commandbox@v2.0.1
  with:
    forgeboxAPIKey: my-token
```

Install a specific version of CommandBox

```yaml
- name: Setup CommandBox with specific version
  uses: Ortus-Solutions/setup-commandbox@v2.0.1
  with:
    version: 5.9.1
```
