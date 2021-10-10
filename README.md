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
  
- Script only returns boot drive, would be nice to return 2nd drive if available
   (I think using -eq "D:" would work pretty consistently, hopefully I will work on a system soon to confirm this.)
  
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
   <br>(use -Path flag to dictate this output to another location)
   
  Get-WmiObject win32_videocontroller call now uses $_.Name vs $_.Description for more consistent results
  
  Removed activation check and replaced with ms-settings:activation
 
   <hr><hr>
  
  <u>Change-Log 9/11/21</u>
  
  What an exciting Week!
  
  overcame unnecessary spaces after variable calls using $($_.<i>varName</i>) 
    <br> this saves a lot of work and has a lot of potential for the future of this project.
    
  Get-Ciminstance Win32_OperatingSystem | % caption added to determine windows 10 home / pro
   
  added get-date to the end of tech infovsection for easier identification in transcript.
   
   <hr><hr>
  
  <u>Change-Log 9/19/21</u>
 
  Get-WmiObject Win32_physicalMemoryArray | % {$_.Memorydevices} added to return available slots
  
  [math]::Round() used to round out screen size on laptop edition.
  
  Minor gramatical fixes. Capitalizing and indenting for cleaner code.
  
     <hr><hr>
  
  <u>Change-Log 9/26/21</u>
 
  .Replace() used to clean up cpu and video controller output
  
  Minor gramatical fixes. Capitalizing and indenting for cleaner code.
  
   <hr><hr>
  
  <u>Change-Log 10/10/21</u>
   
  Replaced all Select-Object with ? and Foreach-Object with % for consistency.

  Added if statements for error catch to drive type and video controller.
   (Video controller error catch is set specificaly to intel products.)
  
  
  
  
