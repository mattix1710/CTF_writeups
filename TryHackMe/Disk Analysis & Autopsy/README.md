# Disk Analysis & Autopsy

- [Link to the room](https://tryhackme.com/room/autopsy2ze0)
- second title: **BTAUTOPSY2**

## Intro
> In the attached VM, there is an Autopsy case file and its corresponding disk image. After loading the .aut file, make sure to re-point Autopsy to the disk image file.
> 
> Ingest Modules were already ran for your convenience.
> 
> Your task is to perform a manual analysis of the artifacts discovered by Autopsy to answer the questions below.
> 
> This room should help to reinforce what you learned in the Autopsy room. Have fun investigating!

## Solution
1. Q1 - ...
2. Q7 - What is the name of the network card on this computer?
   1. Via `Extracted Content` we can open the `Operating System Information` bookmark and then `SOFTWARE` source file. Double click on that will lead to systems *ROOT* location.
   2. Next, choose `Application` bookmark and go to location `Microsoft/Windows NT/CurrentVersion/NetworkCards/2`
   3. Flag is:
      1. <details>
            <center><b>Intel(R) PRO/1000 MT Desktop Adapter</b></center>
         </details>
3. Q9 - A user bookmarked a Google Maps location. What are the coordinates of the location?
   1. Coordinates can be easily found in the `Results/Extracted Content` location. They are placed in `Web Bookmarks` and `Web History`.
   2. For the flag it is necessary to copy the text 1:1:
      1. <details>
            <center><b>12°52'23.0"N 80°13'25.0"E</b></center>
         </details>
4. Q11 - A user had a file on her desktop. It had a flag but she changed the flag using PowerShell. What was the first flag?
   1. It is necessary to browse through all the users `AppData/Roaming/Microsoft/Windows/PowerShell/PSReadLine` locations.
   2. Flag can be found in:
      1. <details>
            <center>shreya: <b>flag{HarleyQuinnForQueen}</b></center>
         </details>