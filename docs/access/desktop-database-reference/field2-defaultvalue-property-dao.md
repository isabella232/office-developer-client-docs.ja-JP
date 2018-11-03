---
title: Field2.DefaultValue プロパティ (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 683255f8bc425ba5d8d2cdf4c66bc2ff16eec43c
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937674"
---
# <a name="field2defaultvalue-property-dao"></a>Field2.DefaultValue プロパティ (DAO)

**適用されます**Access 2013、Office 2013。

**Field2** オブジェクトの既定値を設定または取得します。 [**Fields**](fields-collection-dao.md) コレクションに追加されていない **Field2** オブジェクトの場合、このプロパティは値の取得および設定が可能です (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。既定値

*式***Field2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、最大 255 文字の文字列データ型 ( **String**) です。文字列または式を指定できます。プロパティの設定値が式の場合、ユーザー定義関数、Microsoft Access データベース エンジン SQL の集計関数、またはクエリ、フォーム、その他の **Field2** オブジェクトへの参照を含めることはできません。

> [!NOTE]
> [!メモ] **TableDef** オブジェクトで **Field2** オブジェクトの **DefaultValue** プロパティを "GenUniqueID( )" と呼ばれる特殊な値に設定することもできます。これにより、新規レコードを追加または作成すると、このフィールドに乱数が割り当てられ、各レコードに一意の識別子が設定されます。フィールドの **Type** プロパティは長整数型 ( **Long**) である必要があります。

**DefaultValue** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fields コレクションの所属先</p></th>
<th><p>DefaultValue プロパティの使用</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Index オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="even">
<td><p>QueryDef オブジェクト</p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p>Recordset オブジェクト</p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="even">
<td><p>Relation オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="odd">
<td><p>TableDef オブジェクト</p></td>
<td><p>値の取得および設定が可能です。</p></td>
</tr>
</tbody>
</table>


新しいレコードが作成されると、 **DefaultValue** プロパティの設定値は、フィールドの値として自動的に入力されます。 **Value** プロパティを設定することにより、フィールド値を変更できます。

**DefaultValue** プロパティは、オートナンバ型 ( **AutoNumber**) とロング バイナリ型 ( **Long Binary** ) のフィールドには適用されません。

## <a name="example"></a>例

次の使用例は、 **DefaultValue** プロパティを使用して、ユーザーに入力を要求するときに、フィールドの通常の値を通知するために表示します。また、他に入力がない場合に、 **DefaultValue** が使用されて新しいレコードにデータが設定される方法を示します。このプロシージャを実行するには、DefaultPrompt 関数が必要です。

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```
