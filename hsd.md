# Harmonia Standards Document (HSD)

The Harmonia Standards Document shall be a project to track feature or system implementations within HSW, modules that follow the spec can make note of it by specifying which standard it was implementing:

```lua
-- X-HSD: 1

... -- the module's implementation
```

The purpose of this project is to track ideas, their implementation and any subsequent system changes to ensure that they remain documented for intent.

## Headers

### X-HSD

The only header needed for now.

```
X-HSD: <ID>[, <ID>]
X-HSD: 1
X-HSD: 1, 2, 3
```
