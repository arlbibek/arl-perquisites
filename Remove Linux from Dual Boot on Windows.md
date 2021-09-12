# Remove Linux from Dual Boot on Windows

## After you delete your Linux Partition from Windows 10 do following things

1. Open Command Prompt (CMD) _(as Administrator)_
2. Type following commands:

    \# list all hard drives on your pc and select disk you want to select (in my case '0')

    ```cmd
    diskpart
    list disk
    select disk 0
    ```

    \# display your selected disk's partition info and select where the Volume 'Info' is labeled as 'System' (in my case '2')

    ```cmd
    list volume
    select volume 2
    ```

    \# assign letter 'Z' or similar to the selected volume and exit diskpart

    ```cmd
    assign letter=Z
    exit
    ```

3. Now, Go to 'This PC' using File Explorer, you shall see 'Local Disk (Z:)' mounted to you computer.
4. Again, Open CMD as Administrator
5. Type following commands:

    \# list all directories in the 'Z' and navigate to the 'EFI' directory and list directories there

    ```cmd
    Z:
    dir
    cd EFI
    dir
    ```

    \# remove os files (in my case `kali-linux`) _[Be Cautious! Not to remove anything important.)_

    ```cmd
    rmdir /S kali-linux
    ```

6. Restart your pc and you shall boot into Windows.

\# That is all.
