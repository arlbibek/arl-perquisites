# Kali Linux Full Screen in VirtualBox

1. Open VirtualBox
2. Boot to your kali linux
    From Status Bar go to: **Devices** >> **Insert Guest Additional CD image**
    _(A removable volume (ISO CD Image) should appear in your desktop.*)_
3. Open and Copy all contents of ISO file to any location (Desktop).
4. Open terminal on the folder you copied these file and enter following commands as root user.

   ```sh
   chmod +x VBoxLinuxAdditions.run
   ./VBoxLinuxAdditions.run
   ```

5. Reboot
6. Done!
7. Additionally, Remove all the copied files and Unmount/Eject the iso file.

> Reference: [https://www.youtube.com/watch?v=6LaHG8SC8n4](https://www.youtube.com/watch?v=6LaHG8SC8n4)

---
\# That is all.
