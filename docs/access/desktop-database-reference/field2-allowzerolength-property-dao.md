---
title: Field2.AllowZeroLength プロパティ (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: d3795634-527f-b4c5-b606-50f9945cac12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834791(v=office.15)
ms:contentKeyID: 48547908
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 690a39bd65494e10f4e7d1cdeb047eeb881004b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606738"
---
# <a name="field2allowzerolength-property-dao"></a>Field2.AllowZeroLength プロパティ (DAO)


**適用先**: Access 2013、Office 2013


長さ 0 の文字列 ("") が **[、Text](field-value-property-dao.md)** または Memo データ型 (Microsoft Access ワークスペースのみ) を持つ **Field2** オブジェクトの Value プロパティに対して有効な設定であるかどうかを示す値を設定または返します。

## <a name="syntax"></a>構文

*式* .AllowZeroLength

*式***Field2** オブジェクトを表す変数。

## <a name="remarks"></a>注釈

**Fields** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。

**Fields** コレクションに追加されると、**AllowZeroLength** プロパティを使用できるかどうかは、次の表に示すように、**Fields** コレクションを含むオブジェクトによって異なります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fields コレクションの所属先</p></th>
<th><p>AllowZeroLength プロパティの使用</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> オブジェクト</p></td>
<td><p>非サポート</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
</tbody>
</table>


このプロパティを **[Required](field-required-property-dao.md)** 、 **[ValidateOnSet](field-validateonset-property-dao.md)** プロパティまたは **[ValidationRule](field-validationrule-property-dao.md)** プロパティと共に使用して、フィールドの値を検証できます。

## <a name="example"></a>例

次の使用例では、 **AllowZeroLength** プロパティにより、ユーザーは **Field2** オブジェクトの値を空の文字列に設定できます。こうすると、ユーザーはデータが認識されていないレコードとデータが適用されていないレコードを区別できます。

```vb
    Sub AllowZeroLengthX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strInput As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     ' Create a new Field object and append it to the Fields 
     ' collection of the Employees table. 
     Set fldTemp = tdfEmployees.CreateField("FaxPhone", _ 
     dbText, 24) 
     fldTemp.AllowZeroLength = True 
     tdfEmployees.Fields.Append fldTemp 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Get user input. 
     .Edit 
     strMessage = "Enter fax number for " & _ 
     !FirstName & " " & !LastName & "." & vbCr & _ 
     "[? - unknown, X - has no fax]" 
     strInput = UCase(InputBox(strMessage)) 
     If strInput <> "" Then 
     Select Case strInput 
     Case "?" 
     !FaxPhone = Null 
     Case "X" 
     !FaxPhone = "" 
     Case Else 
     !FaxPhone = strInput 
     End Select 
     
     .Update 
     
     ' Print report. 
     Debug.Print "Name - Fax number" 
     Debug.Print !FirstName & " " & !LastName & " - "; 
     
     If IsNull(!FaxPhone) Then 
     Debug.Print "[Unknown]" 
     Else 
     If !FaxPhone = "" Then 
     Debug.Print "[Has no fax]" 
     Else 
     Debug.Print !FaxPhone 
     End If 
     End If 
     
     Else 
     .CancelUpdate 
     End If 
     
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     tdfEmployees.Fields.Delete fldTemp.Name 
     dbsNorthwind.Close 
     
    End Sub
```
