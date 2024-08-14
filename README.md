# zed_golangci_lint

## Usage

1. **Optional** - Install the golangci-lint-langserver binary. For example, using brew (macOS):

```shell
brew install golangci-lint-langserver
```

2. Add the following to your settings:

```json
"lsp": {
  "golangci-lint": {
    "initialization_options": {
      "command": [
        "golangci-lint",
        "run",
        "--enable-all",
        "--disable",
        "lll",
        "--out-format",
        "json",
        "--issues-exit-code=1"
      ]
    }
  }
},
"languages": {
  "Go": {
    "language_servers": ["gopls", "golangci-lint"]
  }
}
```
