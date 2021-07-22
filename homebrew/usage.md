# Usage

To install a package \(or **Formula** in Homebrew vocabulary\) simply type:

```bash
brew install <formula>
```

To update Homebrew's directory of formulae, run:

```bash
brew update
```

**Note**: If that command fails you can manually download the directory of formulas like this:

```bash
cd /usr/local/Homebrew/
git fetch origin
git reset --hard origin/master
```

To see if any of your formulas need to be updated:

```bash
brew outdated
```

To update a formula:

```bash
brew upgrade <formula>
```

Homebrew keeps older versions of formulas installed on your system, in case you want to roll back to an older version. That is rarely necessary, so you can do some cleanup to get rid of those old versions:

```bash
brew cleanup
```

If you want to see what formulae Homebrew would delete _without actually deleting them_, you can run:

```bash
brew cleanup --dry-run
```

To see what you have installed \(with their version numbers\):

```bash
brew list --versions
```

To search for formulas you run:

```bash
brew search <formula>
```

To get more information about a formula you run:

```bash
brew info <formula>
```

To uninstall a formula you can run:

```bash
brew uninstall <formula>
```

