---
<span data-ttu-id="d760e-101"><<<<<<< ヘッド タイトル: タイプ プロパティの使用例 (VB) の (プロパティ) TOCTitle: タイプ プロパティの使用例 (VB) の (プロパティ) === タイトル: タイプ プロパティの使用例 (VB) の (プロパティ) TOCTitle: タイプ プロパティの使用例 (VB) の (プロパティ)</span><span class="sxs-lookup"><span data-stu-id="d760e-101"><<<<<<< HEAD title: Type Property Example (Property) (VB) TOCTitle: Type Property Example (Property) (VB) ======= title: Type property example (Property) (VB) TOCTitle: Type property example (Property) (VB)</span></span>
>>>>>>> <span data-ttu-id="d760e-102">マスターの ms:assetid: b3fecd24-e15a-3216-e2c8-0f4ce5655b9c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249858(v=office.15) ms:contentKeyID: 48547209 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="d760e-102">master ms:assetid: b3fecd24-e15a-3216-e2c8-0f4ce5655b9c ms:mtpsurl: https://msdn.microsoft.com/library/JJ249858(v=office.15) ms:contentKeyID: 48547209 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="d760e-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="d760e-103"><<<<<<< HEAD</span></span>
# <a name="type-property-example-property-vb"></a><span data-ttu-id="d760e-104">Type プロパティの使用例 (Property) (VB)</span><span class="sxs-lookup"><span data-stu-id="d760e-104">Type Property Example (Property) (VB)</span></span>
=======
# <a name="type-property-example-property-vb"></a><span data-ttu-id="d760e-105">プロパティの使用例 (VB) の (プロパティ) を入力します。</span><span class="sxs-lookup"><span data-stu-id="d760e-105">Type property example (Property) (VB)</span></span>
>>>>>>> <span data-ttu-id="d760e-106">master</span><span class="sxs-lookup"><span data-stu-id="d760e-106">master</span></span>


<span data-ttu-id="d760e-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d760e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d760e-p101">この例では、[Type](type-property-ado.md) プロパティの機能を示します。この例は、 [Properties](properties-collection-ado.md) や [Fields](fields-collection-ado.md) などのコレクションの名前やデータ型の一覧を示すユーティリティのモデルです。</span><span class="sxs-lookup"><span data-stu-id="d760e-p101">This example demonstrates the [Type](type-property-ado.md) property. It is a model of a utility for listing the names and types of a collection, like [Properties](properties-collection-ado.md), [Fields](fields-collection-ado.md), etc.</span></span>

<span data-ttu-id="d760e-p102">[Recordset](recordset-object-ado.md) を開いて **Properties** コレクションにアクセスする必要はなく、 **Recordset** オブジェクトのインスタンスを作成すると、このコレクションが生成されます。ただし、 [CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定すると、動的プロパティが **Recordset** オブジェクトの **Properties** コレクションに追加され、さらに高度な例を作成できます。わかりやすくするために、ここでは明示的に [Item](item-property-ado.md) プロパティを使用して、各 [Property](property-object-ado.md) オブジェクトにアクセスしています。</span><span class="sxs-lookup"><span data-stu-id="d760e-p102">We do not need to open the [Recordset](recordset-object-ado.md) to access its **Properties** collection; they come into existence when the **Recordset** object is instantiated. However, setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** adds several dynamic properties to the **Recordset** object's **Properties** collection, making the example a little more interesting. For sake of illustration, we explicitly use the [Item](item-property-ado.md) property to access each [Property](property-object-ado.md) object.</span></span>

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

