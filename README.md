# vscode-settings

## Automatic

If you are looking forward to an easy one-stop tool to do it for you, I would suggest you to look into the Settings Sync extension.

It will allow:

1) Export of your configuration and extensions
2) Share it with coworkers and teams. You can update the configuration. Their settings will auto updated.

## Manual

1) Make sure you have the most current version of Visual Studio Code. If you install via a company portal, you might not have the most current version.

2) On machine A

 Unix:
  
```bash
code --list-extensions | xargs -L 1 echo code --install-extension
```

 Windows (PowerShell, e. g. using Visual Studio Code's integrated Terminal):

```bash
code --list-extensions | % { "code --install-extension $_" }
```

3) Copy and paste the echo output to machine B

Sample output

```bash
code --install-extension Angular.ng-template
code --install-extension DSKWRK.vscode-generate-getter-setter
code --install-extension EditorConfig.EditorConfig
code --install-extension HookyQR.beautify
```

Please make sure you have the code command line installed. For more information, please visit Command Line Interface (CLI).
