### To encode file text with base64 
$Base64 = [System.Convert]::ToBase64String([System.Text.Encoding]::Unicode.GetBytes([System.IO.File]::ReadAllText("script.ps1")))

### To write encoded string to file 
$Base64 > base64script.txt

### To execute base64 encoded script 
powershell -EncodedCommand $Base64
powershell -EncodedCommand .\base64script.txt

