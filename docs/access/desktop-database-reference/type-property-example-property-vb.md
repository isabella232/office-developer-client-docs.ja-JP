---
title: Type プロパティの使用例 (Property) (VB)
TOCTitle: Type property example (Property) (VB)
ms:assetid: b3fecd24-e15a-3216-e2c8-0f4ce5655b9c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249858(v=office.15)
ms:contentKeyID: 48547209
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 870b68bd43ed12e4d74a9d9f1c1c0887fdb22f85
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885697"
---
# <a name="type-property-example-property-vb"></a>Type プロパティの使用例 (Property) (VB)


**適用されます**Access 2013、Office 2013。

この例では、[Type](type-property-ado.md) プロパティの機能を示します。この例は、 [Properties](properties-collection-ado.md) や [Fields](fields-collection-ado.md) などのコレクションの名前やデータ型の一覧を示すユーティリティのモデルです。

[Recordset](recordset-object-ado.md) を開いて **Properties** コレクションにアクセスする必要はなく、 **Recordset** オブジェクトのインスタンスを作成すると、このコレクションが生成されます。ただし、 [CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定すると、動的プロパティが **Recordset** オブジェクトの **Properties** コレクションに追加され、さらに高度な例を作成できます。わかりやすくするために、ここでは明示的に [Item](item-property-ado.md) プロパティを使用して、各 [Property](property-object-ado.md) オブジェクトにアクセスしています。

```vb 
 
'BeginTypePropertyVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset variables 
 Dim rst As ADODB.Recordset 
 Dim prop As ADODB.Property 
 ' property variables 
 Dim ix As Integer 
 Dim strMsg As String 
 
 ' create client-side recordset 
 Set rst = New ADODB.Recordset 
 rst.CursorLocation = adUseClient 
 ' enumerate property types 
 For ix = 0 To rst.Properties.Count - 1 
 Set prop = rst.Properties.Item(ix) 
 Select Case prop.Type 
 Case adBigInt 
 strMsg = "adBigInt" 
 Case adBinary 
 strMsg = "adBinary" 
 Case adBoolean 
 strMsg = "adBoolean" 
 Case adBSTR 
 strMsg = "adBSTR" 
 Case adChapter 
 strMsg = "adChapter" 
 Case adChar 
 strMsg = "adChar" 
 Case adCurrency 
 strMsg = "adCurrency" 
 Case adDate 
 strMsg = "adDate" 
 Case adDBDate 
 strMsg = "adDBDate" 
 Case adDBTime 
 strMsg = "adDBTime" 
 Case adDBTimeStamp 
 strMsg = "adDBTimeStamp" 
 Case adDecimal 
 strMsg = "adDecimal" 
 Case adDouble 
 strMsg = "adDouble" 
 Case adEmpty 
 strMsg = "adEmpty" 
 Case adError 
 strMsg = "adError" 
 Case adFileTime 
 strMsg = "adFileTime" 
 Case adGUID 
 strMsg = "adGUID" 
 Case adIDispatch 
 strMsg = "adIDispatch" 
 Case adInteger 
 strMsg = "adInteger" 
 Case adIUnknown 
 strMsg = "adIUnknown" 
 Case adLongVarBinary 
 strMsg = "adLongVarBinary" 
 Case adLongVarChar 
 strMsg = "adLongVarChar" 
 Case adLongVarWChar 
 strMsg = "adLongVarWChar" 
 Case adNumeric 
 strMsg = "adNumeric" 
 Case adPropVariant 
 strMsg = "adPropVariant" 
 Case adSingle 
 strMsg = "adSingle" 
 Case adSmallInt 
 strMsg = "adSmallInt" 
 Case adTinyInt 
 strMsg = "adTinyInt" 
 Case adUnsignedBigInt 
 strMsg = "adUnsignedBigInt" 
 Case adUnsignedInt 
 strMsg = "adUnsignedInt" 
 Case adUnsignedSmallInt 
 strMsg = "adUnsignedSmallInt" 
 Case adUnsignedTinyInt 
 strMsg = "adUnsignedTinyInt" 
 Case adUserDefined 
 strMsg = "adUserDefined" 
 Case adVarBinary 
 strMsg = "adVarBinary" 
 Case adVarChar 
 strMsg = "adVarChar" 
 Case adVariant 
 strMsg = "adVariant" 
 Case adVarNumeric 
 strMsg = "adVarNumeric" 
 Case adVarWChar 
 strMsg = "adVarWChar" 
 Case adWChar 
 strMsg = "adWChar" 
 Case Else 
 strMsg = "*UNKNOWN*" 
 End Select 
 'show results 
 Debug.Print "Property " & ix & ": " & prop.Name & _ 
 ", Type = " & strMsg 
 Next ix 
 
 ' clean up 
 Set rst = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 Set rst = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndTypePropertyVB 
```

