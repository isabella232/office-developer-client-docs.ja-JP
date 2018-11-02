---
title: Field.Required プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25ba678f759fefa460dd505cded6e05b3e96fdf5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928356"
---
# <a name="fieldrequired-property-dao"></a>Field.Required プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

**[Field](field-object-dao.md)** オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。

## <a name="syntax"></a>構文

*式*です。必須

*式***Field**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Fields** コレクションにまだ追加されていない **Field** オブジェクトでは、このプロパティは値の取得および設定が可能です。

**Required** プロパティを使用できるかどうかは、次の表に示すように、 [Fields](fields-collection-dao.md) コレクションが含まれているオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fields コレクションが属するオブジェクト</p></th>
<th><p>Required プロパティの使用</p></th>
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
<td><p>サポートしません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>値の取得および設定が可能です。</p></td>
</tr>
</tbody>
</table>


**Required** プロパティは、 **[AllowZeroLength](field-allowzerolength-property-dao.md)** 、 **[ValidateOnSet](field-validateonset-property-dao.md)** 、または **[ValidationRule](field-validationrule-property-dao.md)** プロパティと共に使用して、該当する [Field](field-value-property-dao.md) オブジェクトの ****Value**** プロパティの設定の妥当性を確認できます。 **Required** プロパティが **False** に設定されている場合、そのフィールドには **null** 値を始め、 **AllowZeroLength** プロパティと **ValidationRule** プロパティの設定で指定される条件を満たす値を指定できます。


> [!NOTE]
> <P>[!メモ] このプロパティを <STRONG>Index</STRONG> オブジェクトまたは <STRONG>Field</STRONG> オブジェクトのいずれかに対して設定できる場合は、 <STRONG>Field</STRONG> オブジェクトに対して設定します。 <STRONG>Field</STRONG> オブジェクトに対するプロパティ設定の妥当性は、 <STRONG>Index</STRONG> オブジェクトより前にチェックされます。</P>



## <a name="example"></a>例

次の使用例は、 **Required** プロパティを使用して、新しいレコードを追加するためにデータを含める必要がある、3 つの異なるテーブルのフィールドをレポート出力します。このプロシージャを実行するには、RequiredOutput プロシージャが必要です。

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

