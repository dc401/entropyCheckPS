# entropyCheckPS
Perform entropy checking for unknown data types on windows local drives or shares in Powershell. Useful for checking for potentially ransomware encrypted files.


20170519 dc - Ransomware Encrypted File Checker v1.0
Recurisvely mows through a unc or file path and inspects entropy against all file types
Any file that is greater than 7/8 scored entropy (randomness) will get passed to file 
magic for further inspecting 'unknown' signatures which raise a high suspicion of
potentially encrypted ransomware files. 

This is a re-write of the script from: https://isc.sans.edu/forums/diary/Using+File+Entropy+to+Identify+Ransomwared+Files/21351/
largely because I couldn't get the original author's script to work through functions.
While his functions seem correct, I could not get proper output returned from standard out variables

This script requires the use of the following:
PowerShell v3 or higher installed
Sysinternals SigCheck64.exe and dependencies in the same folder of script
Gnuwin32 File Magic + Magic DB in the same folder of script

Dennis Chow
dchow[AT]xtecsystems.com
www.xtecsystems.com

No warranties and licensed under GPLv2.
