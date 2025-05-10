# T3 Language Support for VS Code

This extension provides syntax highlighting for the T3 language, which transpiles to TypeScript.

## Features

- Syntax highlighting for T3 files (`.t3` extension)
- Support for T3-specific syntax:
  - Parenthesis-free control statements (`if`, `for`, `while`)
  - Parenthesis-free `switch` statements
  - Equality operators (`==`, `!=`) that transpile to TypeScript's strict equality

## Example

T3 code:

```t3
// T3 style switch statement
const value = 42
switch value {
  case 0: {
    console.log("Zero")
    break
  }
  case 42: {
    console.log("The answer")
    break
  }
  default: {
    console.log("Something else")
  }
}

// T3 style for loop
for let i=0; i<10; i++ {
  if i % 2 == 0 {
    console.log(`${i} is even`)
  }
}
```

Transpiled TypeScript:

```typescript
// T3 style switch statement
const value = 42
switch (value) {
  case 0: {
    console.log("Zero")
    break
  }
  case 42: {
    console.log("The answer")
    break
  }
  default: {
    console.log("Something else")
  }
}

// T3 style for loop
for (let i = 0; i < 10; i++) {
  if (i % 2 === 0) {
    console.log(`${i} is even`)
  }
}
```

## Installation

### From VS Code Marketplace

1. Open VS Code
2. Go to Extensions view (Ctrl+Shift+X)
3. Search for "T3 Language"
4. Click Install

## T3 Language Features

T3 provides a simpler, more concise syntax for TypeScript, with these key differences:

1. **Control structures without parentheses**

   ```t3
   if condition {
     // code
   }
   ```

2. **Switch statements without parentheses**

   ```t3
   switch value {
     // cases
   }
   ```

3. **Equality operators**

   ```t3
   // In T3
   if x == y {
     // code
   }

   // Transpiles to TypeScript
   if (x === y) {
     // code
   }
   ```

4. All other TypeScript features (types, interfaces, etc.) work as expected.

## Requirements

- VS Code 1.100.0 or newer

## Known Issues

Please report any issues on the GitHub repository.

## Release Notes

### 0.1.0

- Initial release
- Support for basic T3 syntax highlighting
- Parenthesis-free control structures

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This extension is licensed under the [Apache 2.0 license.](LICENSE).
