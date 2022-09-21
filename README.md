# practice

## Setup w/ Nix/Poetry/Jupyter/Kats/Prophet 
```zsh
nix flake init --template github:nix-community/poetry2nix
cat '{ pkgs ? import <nixpkgs> {} }: pkgs.mkShell { buildInputs = [ pkgs.python3 pkgs.poetry ]; }' > shell.nix 
nix-shell 
poetry init 
poetry add kats jupyter ipykernel pyobjc 
poetry add pandas@1.3.5 ax-platform@0.2.4 gpytorch@1.6.0 botorch@0.6.2
```
