# T3 Language Support for VS Code

Syntax highlighting for T3 and T3X files in Visual Studio Code.

## Features

- Syntax highlighting for T3 files (`.t3` extension)
- Support for T3-specific syntax:
  - Parenthesis-free control statements (`if`, `for`, `while`)
  - Parenthesis-free `switch` statements
  - Equality operators (`==`, `!=`) that transpile to TypeScript's strict equality

## Usage

After installation, VS Code will automatically apply T3 syntax highlighting to files with .t3 and .t3x extensions.

## File extensions

- Use .t3 for regular T3 files
- Use .t3x for T3 files containing JSX/React components

## Example

### Regular T3 file (.t3):

```t3
if count > 10 {
  console.log("Count is too high")
}

switch status {
  case "loading": {
    showSpinner()
    break
  }
  case "error": {
    showError()
    break
  }
}
```

### T3X file with React components (.t3x):

```t3x
function Button(props: { label: string }) {
  const [count, setCount] = useState(0)

  if count > 10 {
    return <span>Too many clicks!</span>
  }

  return (
    <button onClick={() => setCount(count + 1)}>
      {props.label} ({count})
    </button>
  )
}
```

## Installation

### From VS Code Marketplace

1. Open VS Code
2. Go to Extensions view (Ctrl+Shift+X)
3. Search for "T3 Language"
4. Click Install

## Requirements

- VS Code 1.100.0 or newer

## Known Issues

Please report any issues on the GitHub repository.

## Release Notes

### 0.1.5

- Support for `.t3x`

### 0.1.0

- Initial release
- Support for basic T3 syntax highlighting
- Parenthesis-free control structures

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This extension is licensed under the [Apache 2.0 license.](LICENSE).
