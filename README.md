### This httpyac example is for a server project that serves the Supabase database. 
#### Tokens are stored from the response, in an environment variable, with a set name.
##### If an error occurs, just repeat the step that saves the information to the variable.

Summary:

Use the @name decorator to assign a name. For example:
```bash
# @name Variables
```
Initialize global variables:
```bash
{{
  $global.accessToken=null;
  $global.refreshToken=null;
}}
```
Use global variables even in other .http files:
```bash
# @name me
GET /auth/me
Authorization: Bearer {{$global.accessToken}}
```
