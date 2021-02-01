# Grey_screen_error
 Solution for the error when turning on the camera only a gray screen appears on the windows:
 
1. Open the Windows PowerShell (Admin).

2. Type/paste following and press Enter key:


         Get-AppxPackage -allusers Microsoft.WindowsCamera | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml"}


3. Close Windows PowerShell and verify that the problem has been resolved.

Otherwise, try these steps:

1. Open the Device Manager.

2. Under Imaging devices, right click on your camera device and select Uninstall. Click OK.

3. Then click Action > Scan for hardware changes.

4. Close Device Manager and reboot.
