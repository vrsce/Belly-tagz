# Belly-tagz
**_THANKS FOR STOPPING BY!_**
belly tags script (powershell)


Automates belly-tag info for copy - paste into excel / dymo

Could also be useful for test to buys

*Problems are as follows.*

- Cannot retrieve screen size for laptops

- Get-PhysicalDisk portion also returns external drive
  Trying to isolate by number field is ineffective. Does not appear to be integer or string data-type

- Internet info returns pre-made string as per aci standards, not sure if this can be avoided

- Not sure how to return available display ports (hdmi, vga etc...)

- Not sure how to return battery health. 
  Perhaps Win32_BIOS? Win32_Battery exists but does not provide useful results

