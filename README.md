# CheatSheets
List of things I will need to look up at some time

## npm
### List current installed packages
```bash
npm ls --depth=0
```
### Authentication token error
> Couldn't get an authentication token for {{registry}}.

It is solved deleting user's **_.npmrc_** or deleteing the info inside
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

##
### Debug webview from physical device
1. Connect device to the computer via usb
2. Enable usb debugging on the device
3. Access here: [Chrome inspect devices](http://chrome://inspect/#devices "Chrome inspect devices") (chrome://inspect/#devices)
4. Enable permissions on the popup in the device
5. Inspect desired webview
