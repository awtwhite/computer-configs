# computer-configs
Things used to configure my Mac and Windows computers.

## nvim

Directories where things are in different OS:  
https://neovim.io/doc/user/starting.html#standard-path

Using `NVIM_APPNAME` to launch nvim with different config:  
https://www.youtube.com/watch?v=LkHjJlSgKZY


## Windows context menu

Remove the "show more options" entry to the context menu, then open Command Prompt with admin rights and run the following command:
```bash
reg add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
```

Add the "show more options" entry to the context menu, then open Command Prompt with admin rights and run the following command:
```bash
reg delete "HKEY_CURRENT_USER\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}" /f​
```

## Add "edit/open with nvim" to windows context menu

Import the `edit_with_nvim.reg` into the Registry Editor.

Additionally: If you also want to edit/open with Neovim QT (GUI);  
Import the `edit_with_nvim-qt.reg` into the Registry Editor.
