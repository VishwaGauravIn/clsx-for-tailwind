
# `clsx-for-tailwind` - A Utility for Merging Tailwind CSS Classes

`clsx-for-tailwind` is a lightweight utility function for merging Tailwind CSS classes with conditional class names. It combines the power of `clsx` and `tailwind-merge` to provide an easy way to manage your CSS class names in a dynamic and maintainable way.

## Features

- **Conditional Class Names**: Easily toggle class names based on conditions.
- **Class Name Merging**: Automatically merge Tailwind CSS classes without conflicts.
- **TypeScript Support**: Written in TypeScript for type safety and autocomplete support.

## Installation

To install the package, use npm or yarn:

```bash
npm install clsx-for-tailwind
```

or

```bash
yarn add clsx-for-tailwind
```

## Usage

Import the `cn` function and use it to combine your class names:

```typescript
import { cn } from "clsx-for-tailwind";

const buttonClass = cn("btn", "btn-primary", {
  "btn-large": isLarge,
  "btn-disabled": isDisabled,
});

return <button className={buttonClass}>Click Me</button>;
```

This example demonstrates how to conditionally add `btn-large` and `btn-disabled` classes based on the values of `isLarge` and `isDisabled` variables.

## API

### `cn(...inputs: ClassValue[]): string`

- **inputs**: A list of class names, which can be strings, objects, arrays, or a combination of these.
- **returns**: A single string with all the classes merged and deduplicated.

### Example

```typescript
import { cn } from "clsx-for-tailwind";

const classes = cn(
  "p-4",
  "text-center",
  { "bg-blue-500": isActive, "text-white": isActive },
  ["rounded", "shadow-md"]
);

console.log(classes); // Outputs: "p-4 text-center bg-blue-500 text-white rounded shadow-md"
```

## Development

To contribute to this package or modify it locally, follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/VishwaGauravIn/clsx-for-tailwind.git
```

2. Navigate to the project directory:

```bash
cd clsx-for-tailwind
```

3. Install dependencies:

```bash
npm install
```

4. Build the package:

```bash
npm run build
```

5. Run tests:

```bash
npm test
```

## License

This project is licensed under the AGPL-3.0 License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgements

This package relies on the fantastic work of the following libraries:

- [`clsx`](https://github.com/lukeed/clsx) - A tiny utility for constructing `className` strings conditionally.
- [`tailwind-merge`](https://github.com/dcastil/tailwind-merge) - A utility for merging Tailwind CSS class names.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## Contact

For any questions or support, please open an issue on the [GitHub repository](https://github.com/VishwaGauravIn/clsx-for-tailwind).

