# Haskell Development Environment Setup

`TODO:` Automate this setup with [Docker](https://docker.com/)


## Install the Haskell Platform

Install the [Haskell Platform](https://www.haskell.org/platform) (includes Cabal).


## Install `ghc-mod`

1. Install `ghc-mod` via `stack`:
```
stack install ghc-mod
```
1. Update Cabal:
```
cabal install cabal-install
```
1. Add the directory containing the `ghc-mod` executable to your path (e.g. in your `.zshrc`):
```
export PATH=$PATH:/Users/<YOUR_USERNAME>/.local/bin
```


## Atom Plugins

1. Install Runtime Support For Atom Plugins
```
stack install hoogle pointfree pointful
```
1. Install the following plugins from [atom-haskell](https://atom.io/users/atom-haskell):
* [autocomplete-haskell](https://atom.io/packages/autocomplete-haskell)
* [haskell-ghc-mod](https://atom.io/packages/haskell-ghc-mod)
* [haskell-pointfree](https://atom.io/packages/haskell-pointfree)
* [ide-haskell-cabal](https://atom.io/packages/ide-haskell-cabal)
* [ide-haskell-repl](https://atom.io/packages/ide-haskell-repl)
*. [language-haskell](https://atom.io/packages/language-haskell)
