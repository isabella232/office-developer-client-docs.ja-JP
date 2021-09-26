---
title: Field.Required プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8f62d684d3c33024b4e15d5e8f90e432bfa98b47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622341"
---
# <a name="fieldrequired-property-dao"></a>Field.Required プロパティ (DAO)


**適用先**: Access 2013、Office 2013

**[Field](field-object-dao.md)** オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。

## <a name="syntax"></a>構文

*式* .必須

*expression*: **Field** オブジェクトを表す変数。

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
<th><p>Fields コレクションの所属先</p></th>
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
<td><p>非サポート</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
</tbody>
</table>


**Required** プロパティは、**[AllowZeroLength](field-allowzerolength-property-dao.md)**、**[ValidateOnSet](field-validateonset-property-dao.md)**、または **[ValidationRule](field-validationrule-property-dao.md)** プロパティと共に使用して、該当する **Field** オブジェクトの **[Value](field-value-property-dao.md)** プロパティの設定の妥当性を確認できます。**Required** プロパティが **False** に設定されている場合、そのフィールドには **null** 値を始め、**AllowZeroLength** プロパティと **ValidationRule** プロパティの設定で指定される条件を満たす値を指定できます。


> [!NOTE]
> [!メモ] このプロパティを **Index** オブジェクトまたは **Field** オブジェクトのいずれかに対して設定できる場合は、 **Field** オブジェクトに対して設定します。 **Field** オブジェクトに対するプロパティ設定の妥当性は、 **Index** オブジェクトより前にチェックされます。



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

