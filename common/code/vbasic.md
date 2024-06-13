``` visual-basic
Public Function ComputeVerificationHash(publicKey As String, privateKey As String, parameter As String) As String
    Dim oSHA256 As new System.Security.Cryptography.SHA256Managed
    Dim text as string = "SomeSalt+" & publicKey & "+" & privateKey & "++" & parameter & "+ended"
    Dim bytes as byte() = oSHA256.ComputeHash(System.Text.Encoding.UTF8.GetBytes(text))
    Dim hashString as new System.Text.StringBuilder()
    Dim i As Integer
    For i = 0 To bytes.Length - 1
        hashString.Append(String.Format("{0:x2}", bytes(i)))
    Next i
    ComputeVerificationHash = hashString.ToString()
End Function
```