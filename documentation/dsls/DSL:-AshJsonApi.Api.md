<!--
This file was generated by Spark. Do not edit it by hand.
-->
# DSL: AshJsonApi.Api

The entrypoint for adding JSON:API behavior to an Ash API


## json_api
Global configuration for JSON:API


### Nested DSLs
 * [open_api](#json_api-open_api)


### Examples
```
json_api do
  prefix "/json_api"
  log_errors? true
end

```




### Options

| Name | Type | Default | Docs |
|------|------|---------|------|
| [`router`](#json_api-router){: #json_api-router } | `atom` |  | The router that you created for this Api. Use by test helpers to send requests |
| [`prefix`](#json_api-prefix){: #json_api-prefix } | `String.t` |  | The route prefix at which you are serving the JSON:API |
| [`serve_schema?`](#json_api-serve_schema?){: #json_api-serve_schema? } | `boolean` | `false` | Whether or not create a /schema route that serves the JSON schema of your API |
| [`authorize?`](#json_api-authorize?){: #json_api-authorize? } | `boolean` | `true` | Whether or not to perform authorization for this API |
| [`log_errors?`](#json_api-log_errors?){: #json_api-log_errors? } | `boolean` | `true` | Whether or not to log any errors produced |
| [`include_nil_values?`](#json_api-include_nil_values?){: #json_api-include_nil_values? } | `boolean` | `true` | Whether or not to include properties for values that are nil in the JSON output |


## json_api.open_api
OpenAPI configurations



### Examples
```
json_api do
  ...
  open_api do
    tag "Users"
    group_by :api
  end
end

```




### Options

| Name | Type | Default | Docs |
|------|------|---------|------|
| [`tag`](#json_api-open_api-tag){: #json_api-open_api-tag } | `String.t` |  | Tag to be used when used by :group_by |
| [`group_by`](#json_api-open_api-group_by){: #json_api-open_api-group_by } | `:api \| :resource` | `:resource` | Group by :api or :resource |









<style type="text/css">.spark-required::after { content: "*"; color: red !important; }</style>