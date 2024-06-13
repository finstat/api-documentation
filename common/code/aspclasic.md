``` aspnet
Set asc = CreateObject("System.Text.UTF8Encoding")
Set enc = CreateObject("System.Security.Cryptography.SHA256Managed")

bytes = asc.GetBytes_4("SomeSalt+" & l_strAPIKey  & "+" & l_strPRivateKey & "++" & l_strICO  & "+ended")
bytes = enc.ComputeHash_2((bytes))

hash = ""

For pos = 1 To LenB(bytes)
hash = outstr & LCase(Right("0" & Hex(AscB(MidB(bytes, pos, 1))), 2))
Next
```