---
<<<<<<< ヘッド タイトル: 説明、HelpContext、HelpFile プロパティの使用例 (VB) TOCTitle: 説明、HelpContext、HelpFile、以下、番号、ソース、および SQLState プロパティの使用例 (VB) === タイトル: 説明HelpContext、HelpFile プロパティの使用例 (VB) TOCTitle: 説明、HelpContext、HelpFile、以下、番号、ソース、および SQLState プロパティの使用例 (VB)
>>>>>>> マスターの ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15) ms:contentKeyID: 48544304 ms.date: 2015/09/18 mtps_version: v=office.15
---

<<<<<<< ヘッド
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a>Description、HelpContext、HelpFile、NativeError、Number、Source、および SQLState プロパティの使用例 (VB)
=======
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a>説明、HelpContext、HelpFile、以下、番号、ソース、および SQLState プロパティの使用例 (VB)
>>>>>>> master


**適用されます**Access 2013 |。Office 2013

この例では、エラーを発生させてトラップし、生成された [Error](description-property-ado.md) オブジェクトの [Description](helpcontext-helpfile-properties-ado.md)、[HelpContext](helpcontext-helpfile-properties-ado.md)、[HelpFile](nativeerror-property-ado.md)、[NativeError](number-property-ado.md)、[Number](source-property-ado-error.md)、[Source](sqlstate-property-ado.md)、および [SQLState](error-object-ado.md) プロパティを表示します。

```vb
    'BeginDescriptionVB
    Public Sub Main()
    
        Dim Cnxn As ADODB.Connection
        Dim Err As ADODB.Error
        Dim strError As String
        
        On Error GoTo ErrorHandler
        
        ' Intentionally trigger an error
        Set Cnxn = New ADODB.Connection
        Cnxn.Open "nothing"
        
        Set Cnxn = Nothing
        Exit Sub
    
    ErrorHandler:
    
        ' Enumerate Errors collection and display
        ' properties of each Error object
        For Each Err In Cnxn.Errors
            strError = "Error #" & Err.Number & vbCr & _
                "   " & Err.Description & vbCr & _
                "   (Source: " & Err.Source & ")" & vbCr & _
                "   (SQL State: " & Err.SQLState & ")" & vbCr & _
                "   (NativeError: " & Err.NativeError & ")" & vbCr
            If Err.HelpFile = "" Then
                strError = strError & "   No Help file available"
            Else
                strError = strError & _
                   "   (HelpFile: " & Err.HelpFile & ")" & vbCr & _
                   "   (HelpContext: " & Err.HelpContext & ")" & _
                   vbCr & vbCr
            End If
             
            Debug.Print strError
        Next
    
        Resume Next
    End Sub
    'EndDescriptionVB
```
