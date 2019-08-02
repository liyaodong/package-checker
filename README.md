# package-checker

Check all package version for all package.json founded, useful for maintain same version across your monorepo.

## What's the issue

In monoproject, we may have multiple package.json like this

```
/package.json  // yarn workspace root
    src/
        projectA/package.json
            react  // 16.0.0
        projectA/package.json
            react  // 16.0.1
```

Usually you may want to keep all your package `react` to be same version across all mono repo. but check the package.json manullay is a painful work. This tool is born for help that.

## Usage

- Download the binary file
- `$ package-checker` just run the command on your root folder, if some package version is not same it will print log and return `exit 1;`. otherwire it will return `0`;
