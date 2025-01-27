# Core

Core macros provided by [carapace-spec](https://github.com/carapace-sh/carapace-spec).

## directories

[`$directories`](https://carapace-sh.github.io/carapace/carapace/defaultActions/actionDirectories.html) completes directories.
```yaml
["$directories"]
```

## exec

[`$(<command>)`](https://carapace-sh.github.io/carapace/carapace/defaultActions/actionExecCommand.html) executes given command in a `sh` / `pwsh` shell.

```yaml
["$(echo -e 'a\nb\nc')"]
```

## executables

[`$executables`](https://carapace-sh.github.io/carapace/carapace/defaultActions/actionExecutables.html) completes executables either from [PATH] or given directories.
```yaml
["$executables", "$executables([~/.local/bin])"]
```

## files

[`$files([<suffixes>])`](https://carapace-sh.github.io/carapace/carapace/defaultActions/actionFiles.html) completes files with an optional list of suffixes to filter on.

```yaml
["$files([.go, go.mod, go.sum])"]
```

## message

[`$message(<message>)`](https://carapace-sh.github.io/carapace/carapace/defaultActions/actionMessage.html) adds given error message to completion.

```yaml
["$message(some error)"]
```

## spec

`$spec(<file>)` completes arguments using the given spec file.
This implicitly [disables flag parsing](https://pkg.go.dev/github.com/spf13/cobra#Command) for the corresponding (sub)command.

```yaml
["$spec(example.yaml)"]
```

[PATH]:https://en.wikipedia.org/wiki/PATH_(variable)
