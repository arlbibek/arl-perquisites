# Add 'Open Windows Terminal Here' context menu

1. Set the default directory in Windows Terminal to current directory
   - Open Windows Terminal, click on the drop-down button on the title bar and select "Settings". In the JSON file, add the below line to your default profile.

    ```json
    "startingDirectory": null
    ```

2. Create new Registry (reg) file _(`wt.reg`)_ with following code.

    > Note: Replace `<USER NAME>` with your Windows username

    ```reg
    Windows Registry Editor Version 5.00

    [HKEY_CLASSES_ROOT\Directory\Background\shell\wt]
    @="Open Windows Terminal here"

    [HKEY_CLASSES_ROOT\Directory\Background\shell\wt\command]
    @="C:\\Users\\<USER NAME>\\AppData\\Local\\Microsoft\\WindowsApps\\wt.exe"
    ```

3. Save the file and open on it (`wt.reg`). You will be prompted whether you want to merge the reg file. Click on the `Yes` then the `Ok`.
4. Done!  

## RESOURCES

- Add "Open command window here" context menu items (local user + admin) | [/derdimi/OpenCMD](https://github.com/derdimi/OpenCMD)

---
\# That is all.
