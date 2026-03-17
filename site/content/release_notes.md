# Release notes

## v1.9.0: completion and dependency updates

**Date:** 0001-01-01  
**Version:** 1.9.0

**Summary:** This release includes updates to shell completion behavior, documentation coverage, and dependency and tooling configuration.

### New Features

- Added user guide documentation for repeated flags using `CountVarP`, `StringArrayVarP`, and `StringSliceVarP`.

### Bug Fixes

- Fixed shell completion argument handling by iterating directly over the completions array in bash completion and by quoting and escaping non-first arguments in fish completion requests.

### Additional Changes

- Updated `github.com/spf13/pflag` to v1.0.9 and replaced `ParseErrorsWhitelist` with `ParseErrorsAllowlist`.
- Updated static formatting defaults by converting fixed template and padding values from variables to `const`.
- Updated CI and dependencies by switching to `actions/setup-go` v6 and by migrating from `gopkg.in/yaml.v3` to `go.yaml.in/yaml/v3`.
- Updated `.golangci.yml` to disable the `govet` build tag check to support dual build tag syntax.
