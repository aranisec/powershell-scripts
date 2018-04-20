## Base64 encoding

### To encode file data with base64 
```
$Base64 = [System.Convert]::ToBase64String([System.Text.Encoding]::Unicode.GetBytes([System.IO.File]::ReadAllText("script.ps1")))
```
### To encode text with base64 
```
$Text = ‘This is a secret and should be hidden’
$Bytes = [System.Text.Encoding]::Unicode.GetBytes($Text)
$EncodedText =[Convert]::ToBase64String($Bytes)
$EncodedText
```

### To write encoded string to file 
```$Base64 > base64script.txt```

### To execute base64 encoded script 
```
powershell -EncodedCommand $Base64
powershell -EncodedCommand .\base64script.txt
```
## Base64 decoding
