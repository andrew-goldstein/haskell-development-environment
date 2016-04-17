# Haskell Development Environment Setup

* `TODO:` Automate this setup with [Docker](https://docker.com/)


## Install the Haskell Platform

* Install the [Haskell Platform](https://www.haskell.org/platform) (includes Cabal) for OS X

## Install Stack and Stylish Haskell

* Install [Stack](http://docs.haskellstack.org/en/stable/README/) and [Stylish Haskell](https://github.com/jaspervdj/stylish-haskell) via [Homebrew](http://brew.sh/):
```
brew update                      \
&& brew install haskell-stack    \
&& stack install stylish-haskell
```

## Install `ghc-mod`

Install `ghc-mod` via `stack`, then update Cabal and your `$PATH`:

### Install `ghc-mod` via `stack`
```
stack install ghc-mod
```
### Update Cabal
```
cabal update
cabal install cabal-install
```
### Update Your `$PATH`
Add the directory containing the `ghc-mod` executable to your path (e.g. in your `.zshrc`):
```
export PATH=$PATH:/Users/<YOUR_USERNAME>/.local/bin
```


## Install Atom Plugins

Install runtime support for Atom plugins, and then install the plugins themselves:

### Install Runtime Support For Atom Plugins
```
stack install hoogle pointfree pointful
```

### Install Plugins

Install the following plugins from [atom-haskell](https://atom.io/users/atom-haskell):


* [autocomplete-haskell](https://atom.io/packages/autocomplete-haskell)
* [haskell-ghc-mod](https://atom.io/packages/haskell-ghc-mod)
* [haskell-pointfree](https://atom.io/packages/haskell-pointfree)
* [ide-haskell-cabal](https://atom.io/packages/ide-haskell-cabal)
* [ide-haskell-repl](https://atom.io/packages/ide-haskell-repl)
* [language-haskell](https://atom.io/packages/language-haskell)


## Configure Atom Plugins

In Atom > Preferences... > Packages:

Disable the following plugins (yes, you just installed them):

```
ide-haskell-cabal
ide-haskell-hasktags
```

Configure settings for the following plugins:

### `haskell-ghc-mod`

* Change `On Mouse Hover Show` to `Type`
* Uncheck `Use Linter` (resist the urge to leave this enabled)

### `ide-haskell`

* Check the `On Save Prettify` setting
