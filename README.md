# CheatSheets
List of things I will need to look up at some time

## npm
### List current installed packages
```bash
npm ls --depth=0
```

## git
### Remove last commit
```bash
git reset --hard HEAD~1
```

##
### Debug webview from physical device
1. Connect device to the computer via usb
2. Enable usb debugging on the device
3. Access here: [Chrome inspect devices](chrome://inspect/#devices "Chrome inspect devices")
4. Enable permissions on the popup in the device
5. Inspect desired webview
