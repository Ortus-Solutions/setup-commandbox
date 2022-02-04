# setup-commandbox

Sets up [CommandBox CLI](https://www.ortussolutions.com/products/commandbox) for GitHub Actions.

## Inputs

- `forgeboxAPIKey` - If added to the action, we will seed it in CommandBox for you.
- `installGlobalDependencies` - Defaults to false which installs the following dependencies for you: `commandbox-cfconfig,commandbox-dotenv`
- `install` - If added, a comma-delmitted list of packages to install upon setup for you.
- `version` - The CommandBox version to install, if not passed we use the latest stable.

## Usage

Simple usage:

```yaml
- name: Setup CommandBox
  uses: Ortus-Solutions/setup-commandbox@v1.0.0
```

No Global Dependencies:

```yaml
- name: Setup CommandBox
  uses: Ortus-Solutions/setup-commandbox@v1.0.0
  with:
    installGlobalDependencies: true
```

With ForgeBox Token

```yaml
- name: Setup CommandBox With ForgeBox Key
  uses: Ortus-Solutions/setup-commandbox@v1.0.0
  with:
    forgeboxAPIKey: my-token
```

Install a specific version of CommandBox

```yaml
- name: Setup CommandBox With ForgeBox Key
  uses: Ortus-Solutions/setup-commandbox@v1.0.0
  with:
    version: 5.0.0
```
