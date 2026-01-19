# CH2 -- variables
## CH2-1 -- define a variable
To define a variable, define a block with `variable` type.

syntax:

```
# define a variable named `<variable-name>` with type `<variable-type>` and default value `<variable-value>`
variable "<variable-name>" {
  type    = <variable-type>
  default = <variable-value>
}
```

Replace `<variable-name>` to `variable name`, `<variable-type>` to `variable type`, and `<variable-value>` to default value.

## CH2-2 -- access a vairable
Since all defined variables will be stored in `var` object, to access a variable named `<variable-name>`

```
var.<variable-name>
```

Replace `<variable-name>` to `variable name`

| attributes | description |
| :-- | :-- |
| `type` | specific the type of the variable |
| `default` | default value |
| `description` | the description of the variable |
| `sensitive` | If true, it is NOT shown in log file |

| subsection | description |
| :-- | :-- |
| `validation` | defines the validation rule. |

## CH2-3 -- available type
A variable in Terraform can be primitive type

+ string : string in `C#`
+ number : integer in `C#` + double in `C#`
+ bool : bool in `C#`
+ object : object in `C#`

or data type (non-primitive type)

+ list(T) : List<T> in `C#` where T is one of accepted type in Terraform.
+ map(T) : `Dictionary<string,T>` in `C#` where T is one of accepted type in Terraform.
