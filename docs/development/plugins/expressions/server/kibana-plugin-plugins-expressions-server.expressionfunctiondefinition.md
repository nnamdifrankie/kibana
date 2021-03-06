<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [kibana-plugin-plugins-expressions-server](./kibana-plugin-plugins-expressions-server.md) &gt; [ExpressionFunctionDefinition](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.md)

## ExpressionFunctionDefinition interface

`ExpressionFunctionDefinition` is the interface plugins have to implement to register a function in `expressions` plugin.

<b>Signature:</b>

```typescript
export interface ExpressionFunctionDefinition<Name extends string, Input, Arguments extends Record<string, any>, Output, Context extends ExecutionContext = ExecutionContext> extends PersistableStateDefinition<ExpressionAstFunction['arguments']> 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [aliases](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.aliases.md) | <code>string[]</code> |  What is this? |
|  [args](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.args.md) | <code>{</code><br/><code>        [key in keyof Arguments]: ArgumentType&lt;Arguments[key]&gt;;</code><br/><code>    }</code> | Specification of arguments that function supports. This list will also be used for autocomplete functionality when your function is being edited. |
|  [context](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.context.md) | <code>{</code><br/><code>        types: AnyExpressionFunctionDefinition['inputTypes'];</code><br/><code>    }</code> |  |
|  [disabled](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.disabled.md) | <code>boolean</code> | if set to true function will be disabled (but its migrate function will still be available) |
|  [help](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.help.md) | <code>string</code> | Help text displayed in the Expression editor. This text should be internationalized. |
|  [inputTypes](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.inputtypes.md) | <code>Array&lt;TypeToString&lt;Input&gt;&gt;</code> | List of allowed type names for input value of this function. If this property is set the input of function will be cast to the first possible type in this list. If this property is missing the input will be provided to the function as-is. |
|  [name](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.name.md) | <code>Name</code> | The name of the function, as will be used in expression. |
|  [type](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.type.md) | <code>TypeToString&lt;UnwrapPromiseOrReturn&lt;Output&gt;&gt;</code> | Name of type of value this function outputs. |

## Methods

|  Method | Description |
|  --- | --- |
|  [fn(input, args, context)](./kibana-plugin-plugins-expressions-server.expressionfunctiondefinition.fn.md) | The actual implementation of the function. |

