# CheatSheets
List of things I will need to look up at some time

## [CSS](css/css.md)

## npm
### List current installed packages
```bash
npm ls --depth=0
```
### Authentication token error
> Couldn't get an authentication token for {{registry}}.

It is solved deleting user's **_.npmrc_** or deleteing the info inside.

Then execute again:
```bash
vsts-npm-auth -config .npmrc
```

## git
### Remove last commit
```bash
git reset --hard HEAD~1
```
### List branches with commits pending to push
```bash
git log --branches --not --remotes
```
### Generate ssh key
```bash
ssh-keygen -t ed25519 -C "email"
```

## nswag
### Process is terminating due to StackOverflowException.
> Process is terminating due to StackOverflowException.
Look for circular dependency in Json file usually JToken or JObject

## :iphone:
### Debug webview from physical device
1. Connect device to the computer via usb
2. Enable usb debugging on the device
3. Access here on chrome navigation bar:
   ```
   chrome://inspect/#devices
   ```
5. Enable permissions on the popup in the device
6. Inspect desired webview
