# Usage

To install a package \(or **Formula** in Homebrew vocabulary\) simply type:

```text
$ brew install <formula>
```

To update Homebrew's directory of formulae, run:

```text
$ brew update
```

**Note**: If that command fails you can manually download the directory of formulas like this:

```text
$ cd /usr/local/Homebrew/
$ git fetch origin
$ git reset --hard origin/master
```

To see if any of your formulas need to be updated:

```text
$ brew outdated
```

To update a formula:

```text
$ brew upgrade <formula>
```

Homebrew keeps older versions of formulas installed on your system, in case you want to roll back to an older version. That rarely is necessary, so you can do some cleanup to get rid of those old versions:

```text
$ brew cleanup
```

If you want to see what formulas Homebrew would delete _without actually deleting them_, you can run:

```text
$ brew cleanup --dry-run
```

To see what you have installed \(with their version numbers\):

```text
$ brew list --versions
```

To search for formulas you run:

```text
$ brew search <formula>
```

To get more information about a formula you run:

```text
$ brew info <formula>
```

To uninstall a formula you can run:

```text
$ brew uninstall <formula>
```

