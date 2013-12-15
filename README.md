Got
===
A simple, configurable Git wrapper.

> Git it? ***Got** it.* Good!

Installation
------------

1. Clone this repository to your machine. It doesn't really matter where you keep it, as long as it
   will be accessible to you. Let's say you cloned it to `${clone}`.
2. Add an alias to your shell config (e.g., `~/.zshrc` or `~/.bashrc`) so that Got will be invoked
   whenever you use Git: `alias git="${clone}/got"`.

For example:

```shell
mkdir ~/apps && cd ~/apps
git clone https://github.com/cfree3/got.git
echo 'alias git="~/apps/got/got"' >> ~/.zshrc
```

The alias is completely optional. You can run `got` directly if you'd prefer.

Dependencies
------------
Besides a BASH-like `/bin/sh`, the only dependency is [Git][git] itself. `git` should be on your
`${PATH}`.

Configuration
-------------

Got is configured using the standard Git configuration mechanism. You can set these options globally
(`git config --global`) or locally (`git config`). Check out `git help config` for more details
on command syntax.

All Got configuration options are namespaced as `got.*`. Typical Git configuration options are
two-level (`x.y`); but Got configuration options go one step further: `got.x.y`. This allows for
options to be namespaced _within_ the `got` namespace.

In your configuration file, this will look like the following:

```
[got "x"]
    y = value
```

### Options

#### `got.log.graph`

If `true`, `git log` will display a graph by default (the opposite of Git's normal behavior). All
other values are ignored.

License
-------
_Got_ is released under the [MIT][mit] license. Nothing special here.

DISCLAIMER
----------
I give no assurance of this utility's security, and I do not guarantee that it will not zap your
computer and fry your homedir. _Use at your own risk._

Bugs
----
This is a "works-for-me-maybe" project: I do not guarantee that any bugfixing will occur.

[git]: http://git-scm.com
[mit]: http://www.tldrlegal.com/l/MIT
