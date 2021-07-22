# RubyGems

[RubyGems](http://rubygems.org/), the Ruby package manager, should be installed on your machine if you previously have installed Ruby. Verify this by running:

```bash
which gem
```

## Update RubyGems

To update to its latest version with:

```bash
gem update --system
```

## Install gems

To install a _gem_ \(Ruby package\), run:

```bash
gem install <gemname>
```

To install without generating the documentation for each gem \(faster\):

```bash
gem install <gemname> --no-document
```

## List installed gems

```bash
gem list
```

To check if any installed gems are outdated:

```bash
gem outdated
```

## Update installed gems

To update all gems or a particular gem:

```bash
gem update [<gemname>]
```

## Remove old gem versions

RubyGems keeps old versions of gems, so feel free to do some cleaning after updating:

```bash
gem cleanup
```

