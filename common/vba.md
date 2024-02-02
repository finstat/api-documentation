``` visual-basic
Public Function ComputeVerificationHash(publicKey As String, privateKey As String, parameter As String) As String
    Dim oT As Object
    Dim oSHA256 As Object
    Dim TextToHash() As Byte
    Dim bytes() As Byte
 
    Set oT = CreateObject("System.Text.UTF8Encoding")
    Set oSHA256 = CreateObject("System.Security.Cryptography.SHA256Managed")
 
    TextToHash = oT.GetBytes_4("SomeSalt+" & publicKey & "+" & privateKey & "++" & parameter & "+ended")
    bytes = oSHA256.ComputeHash_2(TextToHash)
 
    Dim oD As Object
    Set oD = CreateObject("MSXML2.DOMDocument")
 
    With oD
        .LoadXML "<root />"
        .DocumentElement.DataType = "bin.Hex"
        .DocumentElement.nodeTypedValue = bytes
    End With
    ComputeVerificationHash = Replace(oD.DocumentElement.Text, vbLf, "")
 
    Set oT = Nothing
    Set oSHA256 = Nothing
    Set oD = Nothing
End Function
```