# graphql
## Types
- variables: preceded by $ (ex. $title: String!)
## graphql as Query Language
graphql is parsed into abstract syntax tree validated before the operation runs. curly brackets comes after each operation containing operations' selection sets.
## Root Object Type / Operation Types
### Query
### Mutations
Perform data change that affects the state of the backend data.
#### Syntax
``` graphql
mutation name {
  nameOfFunctionToPerform(args) {
    selection_sets
  }
}
```
- args: optional, but required for best practice. the args can be either variables or static value.
- selections_sets: optional. you can omit parenthesis after the function name if you do not want any selection sets

Example:
``` graphql
mutation createsong {
  addsong(title: "No Scrubs") {
    id
    title
  }
}
```
### Subscription
real-time updates on API schema as fields. unsubscribe by closing the window
## Other Query Language Feature
### Introspection
gives query details about the current API's schema.
