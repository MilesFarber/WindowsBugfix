# As always, make sure you have a backup of everything, and that it's unplugged from the system you're running this on.

```
$url = "https://raw.githubusercontent.com/MilesFarber/WindowsBugfix/Leader/Bugfix.reg"
$tempFile = "$env:TEMP\Bugfix.reg"
Invoke-WebRequest -Uri $url -OutFile $tempFile
Start-Process reg.exe -ArgumentList "import `"$tempFile`"" -Verb RunAs
