# DataFlex-LSP-Workspace
Convenience workspace for building DataFlex-LSP along with related editor extension projects, e.g. VSCode extension.

## Installing
If you just want to install the DataFlex-LSP VSCode extension, you can download a pre-built binary VSCode extension.
The latest pre-built binary release is [v0.8.1](https://github.com/sonnyfalk/dataflex-lsp/releases/tag/v0.8.1), scroll to the bottom of that page and download `vscode-dataflex-win32-x64-0.8.1.vsix`.
In the VSCode Extensions tab, select `Install from VSIX`, and then install the downloaded .vsix file. Now you can open any DataFlex workspace folder, and get full syntax highlighting, code completion, goto definition, etc.

## Building from Source
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

Run `cargo install cargo-make` to install `cargo-make`.

#### 3. Build the workspace
Run `cargo make` to build the workspace and copy the result into the VSCode extension.

#### 4. Test in VSCode
Debug the extension in VSCode by opening `./dataflex-lsp-workspace/vscode-dataflex` and selecting `Run` -> `Start Debugging`. 
