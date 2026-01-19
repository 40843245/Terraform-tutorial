# CH12 -- specifying version
## objectives
You will learn how to 

  + specify required version in Terraform

## CH12-1 -- specify required version in Terraform
Format:

```
<op> <major>.<minor>.<patch>
```

(usually replace `<op>` to `>=`)

or

```
<op> <major>.<minor>
```

(usually replace `<op>` to `~>`)

Replace `<op>` to one of available operators (listed as follows)

Replace `<major>` to major version. MUST be a postive integer.

Replace `<minor>` to minor version. MUST be a nonnegative integer.

Replace `<patch>` to patch version. MUST be a nonnegative integer.

| available operator | description | example | explanation of example |
| :-- | :-- | :-- | :-- |
| `>=` | greater than or equal to the version | `>= 1.5.0` | use version at least `1.5.0` (such as `1.5.0`, `1.5.1`, `1.6.0`, `2.1.0`) |
| `~>` | greater than the version but in same major version | `~> 3.0` | use the version between `3.0` (exclusive) and `3.x` (such as `3.1`, `3.5`). `3.0`, `4.0` is NOT met the required version |
