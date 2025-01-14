# Change Log

## 2.0.1

### Patch Changes

- 546e2b1: Fixed package name in main readme

## 2.0.0

Implements eslint flat config with eslint 9.

**BREAKING CHANGES**: see [the release candidate docs below](https://github.com/IGNE-Agency/code-consistency/blob/main/packages/eslint-config-igne/CHANGELOG.md#200-rc0).

## 2.0.0-rc.0

### Major Changes

- 84247ba: Implements eslint flat config with eslint 9.

  **BREAKING CHANGES**

  - Now using eslint flat config. See the [docs](./README.md) to learn how to update your existing config.
  - **Eslint version >=9** is now required as peerdependency (was 8).
  - **Typescript version >=4.7.4** is now required for typescript projects (was 4.0.0).
  - The package is now in ESM format. There are no IGNE dependents using CJS AFAIK, but if I missed one [let me know](https://github.com/IGNE-Agency/code-consistency/issues).
  - The default eslint config should now be imported like: `import { eslintConfigDefault } from '@igne-agency/eslint-config-igne'`
  - The expo eslint config should now be imported like: `import { eslintConfigExpo } from '@igne-agency/eslint-config-igne'`

  **Additional notes**

  - `tsconfig.json` or `tsconfig.*.json` files should be present in the project root. Amongst other things, these are used for paths (aliases) by the import plugin. Other names/locations are currently not supported, but you can update your local `eslint.config.js`.
    None of the IGNE projects currently use any other tsconfig name or location, so this should not be an issue. Otherwise [let me know](https://github.com/IGNE-Agency/code-consistency/issues).
  - The expo plugin is not updated yet for flat config, so the two [expo rules](https://github.com/expo/expo/tree/main/packages/eslint-plugin-expo/docs/rules) no longer work.
    These are quite minor and should give runtime warnings in development anyway.
  - CJS files now have the global `node`, so no more error for `module` doesn't exist.

## 1.6.0

### Minor Changes

- e42ebf5: Added `react` and `JSX` globals so eslint doesn't complain about typescript references. Fixes #11.

  If you added these globals yourself in your config, you can remove them.

- 2ed5f67: Added typescript-eslint plugin, so consumers don't need to add it themselves anymore. Fixes #12.

---

All entries below this point are pre-[changesets](https://github.com/changesets/changesets)

---

# [1.5.0](https://github.com/IGNE-Agency/code-consistency/compare/@igne-agency/eslint-config-igne@1.0.0...@igne-agency/eslint-config-igne@1.5.0) (2024-07-08)

### Bug Fixes

- also lint jsx files ([b7f6582](https://github.com/IGNE-Agency/code-consistency/commit/b7f658209b76189b8ce84c4dddce9f14c436d005))
- **eslint:** ignore package related files ([7181f2f](https://github.com/IGNE-Agency/code-consistency/commit/7181f2f63a04862be1cc012cb686947205dfb428))
- import rules were not properly exported ([86647b5](https://github.com/IGNE-Agency/code-consistency/commit/86647b5ae22f013036549ae02aabeeb2b48f797b))

### Features

- **eslint:** add expo config ([2e32a22](https://github.com/IGNE-Agency/code-consistency/commit/2e32a22e3f0a1e1bc7abd3c503d567562258a5b9))
- **eslint:** added import sorting ([a76f81b](https://github.com/IGNE-Agency/code-consistency/commit/a76f81b12f16d5a1712557a6958f5a0905d45e80))
- **eslint:** moved rules to separate files ([9ac0ae3](https://github.com/IGNE-Agency/code-consistency/commit/9ac0ae304b5c59f6ed5279632f6f8cd8333d8eaa))

## [1.4.1](https://github.com/IGNE-Agency/code-consistency/compare/@igne-agency/eslint-config-igne@1.4.0...@igne-agency/eslint-config-igne@1.4.1) (2024-07-02)

### Bug Fixes

- **eslint:** ignore package related files ([71550dc](https://github.com/IGNE-Agency/code-consistency/commit/71550dcb19fa7f1cea2cd4f87bde619c6097461f))

# [1.4.0](https://github.com/IGNE-Agency/code-consistency/compare/@igne-agency/eslint-config-igne@1.0.0...@igne-agency/eslint-config-igne@1.4.0) (2024-07-02)

### Bug Fixes

- also lint jsx files ([838e05c](https://github.com/IGNE-Agency/code-consistency/commit/838e05c17a77d703584e25af4fca4d7050e4d63d))
- import rules were not properly exported ([86647b5](https://github.com/IGNE-Agency/code-consistency/commit/86647b5ae22f013036549ae02aabeeb2b48f797b))

### Features

- **eslint:** added import sorting ([a76f81b](https://github.com/IGNE-Agency/code-consistency/commit/a76f81b12f16d5a1712557a6958f5a0905d45e80))
- **eslint:** moved rules to separate files ([9ac0ae3](https://github.com/IGNE-Agency/code-consistency/commit/9ac0ae304b5c59f6ed5279632f6f8cd8333d8eaa))

# [1.3.0](https://github.com/IGNE-Agency/code-consistency/compare/@igne-agency/eslint-config-igne@1.0.0...@igne-agency/eslint-config-igne@1.3.0) (2024-07-02)

### Bug Fixes

- import rules were not properly exported ([baebc38](https://github.com/IGNE-Agency/code-consistency/commit/baebc385d7a17e65949cccd990b2e19d8507abec))

### Features

- **eslint:** added import sorting ([a76f81b](https://github.com/IGNE-Agency/code-consistency/commit/a76f81b12f16d5a1712557a6958f5a0905d45e80))
- **eslint:** moved rules to separate files ([9ac0ae3](https://github.com/IGNE-Agency/code-consistency/commit/9ac0ae304b5c59f6ed5279632f6f8cd8333d8eaa))

# [1.2.0](https://github.com/IGNE-Agency/code-consistency/compare/@igne-agency/eslint-config-igne@1.0.0...@igne-agency/eslint-config-igne@1.2.0) (2024-06-26)

### Features

- **eslint:** added import sorting ([f6439ba](https://github.com/IGNE-Agency/code-consistency/commit/f6439badd2fc33c0d3e92f16573f37804c8d4597))
- **eslint:** moved rules to separate files ([9ac0ae3](https://github.com/IGNE-Agency/code-consistency/commit/9ac0ae304b5c59f6ed5279632f6f8cd8333d8eaa))

# [1.1.0](https://github.com/IGNE-Agency/code-consistency/compare/@igne-agency/eslint-config-igne@1.0.0...@igne-agency/eslint-config-igne@1.1.0) (2024-06-26)

### Features

- **eslint:** moved rules to separate files ([b5e9e86](https://github.com/IGNE-Agency/code-consistency/commit/b5e9e862c3d324c2978ea19aeac3e09a423a6365))
