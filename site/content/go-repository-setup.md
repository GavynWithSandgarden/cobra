# Go repository setup

This page describes a minimal, repeatable setup for a Go repository.

## Prerequisites

- `go`
- `git`

## Initialize the repository

1. Create and enter a new directory.

   ```console
   mkdir example
   cd example
   ```

1. Initialize a Git repository.

   ```console
   git init
   ```

## Initialize the Go module

1. Create a Go module.

   ```console
   go mod init example.com/example
   ```

1. Verify that `go.mod` exists and has a `module` line.

   ```text
   module example.com/example
   ```

## Add a minimal program

1. Create `main.go`.

   ```go
   package main

   import "fmt"

   func main() {
   	fmt.Println("hello")
   }
   ```

1. Build the program.

   ```console
   go build ./...
   ```

1. Run the program.

   ```console
   go run .
   ```

## Add tests

1. Create `main_test.go`.

   ```go
   package main

   import "testing"

   func TestMain(t *testing.T) {
   	// Minimal placeholder test.
   }
   ```

1. Run tests.

   ```console
   go test ./...
   ```

## Apply common project hygiene

1. Format code.

   ```console
   gofmt -w .
   ```

1. Commit the initial baseline.

   ```console
   git add .
   git commit -m "initialize module"
   ```

## Repository-specific notes (this repository)

- Module path in `go.mod`: `github.com/spf13/cobra`
- `go.mod` declares `go 1.15`.
- Test commands referenced in `CONTRIBUTING.md`:
  - `go test ./...`
  - `make test`
  - `make all`

## Related pages

- Cobra user guide: [User Guide](./user_guide.md)