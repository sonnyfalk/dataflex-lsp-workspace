# DataFlex-LSP-Workspace
Convenience workspace for building DataFlex-LSP along with related editor extension projects, e.g. VSCode extension.

## Building
#### 1. Clone required workspace member repos inside, i.e. `dataflex-lsp`, `tree-sitter-dataflex`, `vscode-dataflex`:
```
$ cd dataflex-lsp-workspace
$ git clone https://github.com/sonnyfalk/dataflex-lsp.git
$ git clone https://github.com/sonnyfalk/tree-sitter-dataflex.git
$ git clone https://github.com/sonnyfalk/vscode-dataflex.git
```

For the following structure:
```
./dataflex-lsp-workspace/
./dataflex-lsp-workspace/dataflex-lsp/
./dataflex-lsp-workspace/tree-sitter-dataflex/
./dataflex-lsp-workspace/vscode-dataflex/
```

#### 2. Install cargo-make
This uses [cargo-make](https://crates.io/crates/cargo-make) to build the workspace and copy files into the VSCode extension, so it can be tested in VSCode.

Run `cargo install --force cargo-make` to install `cargo-make`.

#### 3. Build the workspace
Run `cargo make` to build the workspace and copy the result into the VSCode extension.

#### 4. Test in VSCode
Debug the extension in VSCode by opening `./dataflex-lsp-workspace/vscode-dataflex` and selecting `Run` -> `Start Debugging`. 
