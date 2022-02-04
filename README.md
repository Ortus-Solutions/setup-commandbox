# setup-commandbox

Sets up [CommandBox CLI](https://www.ortussolutions.com/products/commandbox) for GitHub Actions.

## Inputs

- `forgeboxAPIKey` - If added to the action, we will seed it in CommandBox for you.

## Usage

Simple usage:

```yaml
- name: Setup CommandBox
  uses: Ortus-Solutions/setup-commandbox@v1.0.0
```

With ForgeBox Token

```yaml
- name: Setup CommandBox With ForgeBox Key
  uses: Ortus-Solutions/setup-commandbox@v1.0.0
  with:
    forgeboxAPIKey: my-token
```
