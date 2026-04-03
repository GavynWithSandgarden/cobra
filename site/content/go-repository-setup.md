# Go repository setup (Cobra)

This page describes how to set up a local working copy of the `github.com/spf13/cobra` Go module.

## Prerequisites

- `go`
- `git`

## Clone the repository

1. Clone the repository.

   ```console
   git clone https://github.com/spf13/cobra
   ```

1. Enter the repository directory.

   ```console
   cd cobra
   ```

## Verify module metadata

1. Open `go.mod`.

1. Confirm the module path.

   ```text
   module github.com/spf13/cobra
   ```

1. Confirm the Go version directive.

   ```text
   go 1.15
   ```

## Run tests

1. Execute tests.

   ```console
   go test ./...
   ```

1. Execute the project test target.

   ```console
   make test
   ```

## Run all checks

1. Execute the full project target.

   ```console
   make all
   ```

## Related pages

- Cobra user guide: [User Guide](./user_guide.md)