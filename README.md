# haskell-template

Haskell project template optimized for a fully reproducible and friendly development environment. Based on Nix + Flakes + VSCode (HLS) + Relude.

## Getting Started

- [Install Nix](https://nixos.org/download.html) & [enable Flakes](https://nixos.wiki/wiki/Flakes)
- Run `nix-shell --run haskell-language-server` to sanity check your environment 
- [Open as single-folder workspace](https://code.visualstudio.com/docs/editor/workspaces#_singlefolder-workspaces) in Visual Studio Code
    - Install the [workspace recommended](https://code.visualstudio.com/docs/editor/extension-marketplace#_workspace-recommended-extensions) extensions
    - <kbd>Ctrl+Shift+P</kbd> to run command "Nix-Env: Select Environment" and select `shell.nix`. The extension will ask you to reload VSCode at the end.
- Press <kbd>Ctrl+Shift+B</kbd> in VSCode, or run `bin/run` (`bin/run-via-tmux` if you have tmux installed) in terminal, to launch Ghcid running your program.

All but the final step need to be done only once.

Then, before using it for real,

- Rename all occurrences of `haskell-template` to `myproject`, as well as rename the cabal file to `myproject.cabal`. 
- Run `git add . && git ci -m rename` followed by `nix develop` (or `bin/run`) to verify that everything continues to work.
