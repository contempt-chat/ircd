# Extended Ban (Extban)
## Introduction
Extban extends the usual nick!ident@host mask for bans (+b), exempts (+e), invites (+I) and reops (+R).
If the nick field starts with an `$`, it will be used for extban instead of nick.

## Syntax
```
$<type>[:parameter]!user@host
```

## Types
| Type  | Description |
| ----- | ----------- |
| a | Matches any user who is logged in to the account specified in the parameter. Wildcards are supported. The parameter can be omitted to match any logged in user.  |

## Examples
```
MODE #test +I $a:patrick!*@*
```
Matches everyone who is logged in with account `patrick`.

```
MODE #test +I $a:pat*!*@*
```
Matches everyone who is logged in with an account whose name starts with `pat`.

```
MODE #test +I $a!*@*
```
Matches everyone who is logged in.

```
MODE #test +I $a!*@127.0.0.1
```
Matches everyone who is logged in and is connecting from `127.0.0.1`.
