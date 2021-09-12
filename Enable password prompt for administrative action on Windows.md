# Enable password prompt for administrative action on Windows

1. Open `Registry Editor`
2. Navigate to:

    ```path
    Computer\HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System
    ```

3. Open `ConsentPromptBehaviorAdmin` and change "Value data" (_from `5`_) to `1` and hit OK.
4. Done!

    > From now on, your computer will ask you to enter the `password`/`PIN` for any administrator action instead of just `Yes`/`No`.

---
\# That is all.
