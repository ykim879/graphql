# graphql
## Types
- variables: preceded by $ (ex. $title: String!)
## Root Object Type
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
