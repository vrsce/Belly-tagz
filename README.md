# Belly-tagz
**_THANKS FOR STOPING BY!_**<br>
belly tags script (powershell)


Automates belly-tag info for copy - paste into excel / dymo

Could also be useful for test to buys

*Problems are as follows.*

- <strike>Cannot retrieve screen size for laptops</strike>

- <strike> Get-PhysicalDisk portion also returns external drive.</strike> <br>
   <strike>Trying to isolate by number field is ineffective. Does not appear to be integer or string data-type</strike>

- Internet info returns pre-made string as per aci standards, not sure if this can be avoided

- Not sure how to return available display ports (hdmi, vga etc...)

- Not sure how to return battery health.<br> 
  Perhaps Win32_BIOS? Win32_Battery exists but does not provide useful results
  
  <hr><hr>
  
  <u>Change-Log 8/25/21</u>
  
  Fun New Headers!
  
  Used -eq instead of = to resolve ram type and activation problems
  
  Resolved external drive issue by isolating first position of ForEach loop through drive types
     (Thanks Lwed for suggesting LogicalDisk over PhysicalDrive)
  
  Implemented WmiMonitorBasicDisplayParams to retrieve screen size (thanks again to Lwed)
  
  Added command to open file explorer to expose script in recent files, and file explorer options to clear it.
  
    
  <hr><hr>
  
  <u>Change-Log 9/4/21</u>
  
  Implemented Start-Transcript with $mod variable to output .txt files of script info
   (use -Path flag to dictate this output to another location)
   
  Get-WmiObject win32_videocontroller call now uses $_.Name vs $_.Description for more consistent results
  
  Removed activation check and replaced with ms-settings:activation
 
 
  
  

