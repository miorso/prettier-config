# `@miorso/prettier-config`

Shared Prettier configuration for consistent code formatting across projects.

## Install

```sh
npm install --save-dev @miorso/prettier-config
```

## Configuration

The following table lists the specific Prettier options this package changes:

| Option        | Value  | Description                                 |
| ------------- | ------ | ------------------------------------------- |
| `printWidth`  | `120`  | Wrap lines exceeding 120 characters.        |
| `useTabs`     | `true` | Use tabs instead of spaces for indentation. |
| `singleQuote` | `true` | Use single quotes instead of double quotes. |

## Usage

Create a `.prettierrc` file in your project and extend the configuration:

```json
"@miorso/prettier-config"
```

Alternatively, you can add it to your `package.json`:

```json
{
	"prettier": "@miorso/prettier-config"
}
```

### Extending the Configuration

If you need to customize specific Prettier options while still using the shared base configuration, you can extend it programmatically by creating a `.prettierrc.mjs` file:

```javascript
import baseConfig from '@miorso/prettier-config';

/** @type {import("prettier").Config} */
const config = {
	...baseConfig,
	semi: false,
};

export default config;
```

> 💡 For detailed Prettier documentation, visit [Prettier's official site](https://prettier.io/).
