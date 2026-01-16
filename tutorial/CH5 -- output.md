# CH5 -- output
## objectives
You will learn how to

  + stream outputs to specific file when automatically executing `*.tf` file

## CH5-1 -- stream outputs to specific file automatically
### resource
To stream outputs to specific file automatically, you can think that it is equivalent to download a file into local device.

To download a file into local device, you can use the resource named `local_file`

```
resource "local_file" "<logic-name>"{
  filename = "<full-name>"
  content  = "<content-that-will-stream-to-specific-file>"
}
```

Replace `<full-name>` to the full name that content will redirect to.

Replace `<content-that-will-stream-to-specific-file>` to content for redirection.

Replace `<logic-name>` to a valid identifier as a logic name of the resource. When the full name (`<full-name>`) is referenced, the logic name will be used.

see examples for more details.
