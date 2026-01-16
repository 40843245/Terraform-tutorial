# CH9 -- configure used resource
## objectives
You will learn how to

  + define components to configure used resource

## CH9-1 -- configure used resource
### `resource` block
To define components that is used by providers (platform and service),

you can use `resource` block.

syntax:

```
resource "<resource-type>" "<local-resource-name>" {
  # ... pass arguments of resource
}
```

Replace `<resource-type>` to the resource type.

Replace `<local-resource-name>` to a descriptive name as an alias of local resource name (used for reference in codespace or configuration file)
