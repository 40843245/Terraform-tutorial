# CH8 -- configure used platform or serivce
## objectives
You will learn how to

  + configure used platform or serivce

## CH8-1 -- configure used platform or serivce
### `provider` block
To configure used platform or serivce, you can use `provider` block

syntax:

```
provider "<provider-name>" {
  # ... tell the Terraform more info it needs about providers info
}
```

Replace `<provider-name>` to the platform name or service name.

Available attributes are listed as follows and provider's own-defined attribute.

| attributes | description |
| :-- | :-- |
| `alias` | The alias of the provider. The alias might be used in resource block (format: `<provider_name>.<alias>`) or in providers subblock in module block (format: `<provider_name>.<alias>`) |
