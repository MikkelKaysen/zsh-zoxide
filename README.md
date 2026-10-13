# zsh-zoxide

A Zsh plugin that initializes [zoxide](https://github.com/ajeetdsouza/zoxide), a smarter `cd` alternative.

## Requirements

- [zoxide](https://github.com/ajeetdsouza/zoxide) must be installed and available on your `$PATH`.

## Installation

### zinit

```zsh
zinit light mikkelkaysen/zsh-zoxide
```

### Oh My Zsh

Clone the repository into your custom plugins directory:

```zsh
git clone https://github.com/mikkelkaysen/zsh-zoxide.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/zsh-zoxide
```

Then add `zsh-zoxide` to your plugins list in `~/.zshrc`:

```zsh
plugins=(... zsh-zoxide)
```

### zimfw

Add the following to your `~/.zimrc`:

```zsh
zmodule mikkelkaysen/zsh-zoxide
```

Then run:

```zsh
zimfw install
```

## Features

When `zoxide` is found on the system, the plugin:

1. Generates a shell init script by running `zoxide init zsh`.
2. Compiles it with `zcompile` for faster sourcing on subsequent shell starts.
3. Caches the compiled init file in the plugin directory (`zoxide-init.zsh`).
4. Re-generates the init file only when it doesn't exist or is older than the `zoxide` binary.
5. Sources the init file to activate the `z` and `zi` commands.

## License

[MIT](./LICENSE) — Copyright (c) 2020 Mikkel Kaysen
