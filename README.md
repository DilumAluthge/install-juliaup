# `install-juliaup`

GitHub Action to install `juliaup`.

When you use this action, it will do three things:

1. Make sure that `juliaup` is available (downloading if if necessary).
2. Use `juliaup` to install the specified version of Julia.
3. Add both `juliaup` and `julia` to the PATH.

## Example usage

To install the latest stable Julia v1:

```yaml
- uses: julia-actions/install-juliaup@latest
  with:
    julia-version: '1'
```

To install a specific Julia version:

```yaml
- uses: julia-actions/install-juliaup@latest
  with:
    julia-version: '1.10.2'
```

If you want alphas for the next upcoming release:

```yaml
- uses: julia-actions/install-juliaup@latest
  with:
    julia-version: 'alpha'
```

In general, if `juliaup add FOO` would have been a valid command on your local machine, then `FOO` is valid value for the `julia-version` input to this action.
