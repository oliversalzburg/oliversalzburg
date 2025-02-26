# Manifest for maintained Projects

## General

- Focus on POSIX. Windows is ignored.

## Consistent tool stack

- Biome
- esbuild
- make
- OpenTofu
- TypeScript
- vite
- yarn

## Consistent entrypoints

- make

### Default (phony) make targets

- _default_ produces clean build (literally `clean` `build`)
- `build` produces build output, acquires dependencies
- `clean` cleans build output
- `docs` builds only the documentation
- `pretty` auto-formats code, applies linter auto-fixes
- `lint` checks the code for common issues
- `test` runs tests
- `run` **might** exist to run the main output

All of these are expected to be phony targets.

Make targets are not duplicated into manifest scripts.

## Consistent CI/CD

- GitHub Workflows/Actions
- Renovate

## Continuously released

- Automatic semantic releases
