# Release notes

## Incoming payload

```json
{
  "Additional Changes": [
    "Command-line flag parsing dependencies were refreshed and modernized to align with current naming and compatibility expectations. The project updated `github.com/spf13/pflag` through v1.0.9 and replaced `ParseErrorsWhitelist` with `ParseErrorsAllowlist`.",
    "Static formatting defaults are now expressed as constants to reduce accidental mutation and improve clarity. Several package-level variables (including `minUsagePadding` and default template/padding values) were converted to `const` with no behavioral change.",
    "CI and build tooling were updated to keep the development pipeline current and compatible. GitHub Actions now uses `actions/setup-go` v6, and the YAML dependency was switched from `gopkg.in/yaml.v3` to `go.yaml.in/yaml/v3`.",
    "Linting configuration was adjusted to avoid false positives when using modern build tag formats. The GolangCI configuration disables the `govet` build tag check to allow dual build tag syntax."
  ],
  "Bug Fixes": [
    "Shell completion now handles arguments more safely and predictably when generating suggestions. Bash completion iterates directly over the completions array (avoiding a subprocess read), and fish completion now properly quotes and escapes non-first arguments in the request command."
  ],
  "New Features": [
    "New documentation explains how to pass the same command-line option multiple times and what results to expect. The user guide now includes examples for repeated flags using `CountVarP` and `StringArrayVarP`/`StringSliceVarP`."
  ]
}

```
