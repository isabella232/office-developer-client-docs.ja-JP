---
title: Field2.Required プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e6d4963ed10f2bf886a7445dfa05f1a3fcef460
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872943"
---
# <a name="field2required-property-dao"></a>Field2.Required プロパティ (DAO)


**適用されます**Access 2013、Office 2013。


**Field2** オブジェクトに非 Null 値が必須かどうかを示す値を設定または取得します。

## <a name="syntax"></a>構文

*式*です。必須

*式***Field2**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

**Fields** コレクションに追加されていない **Field2** オブジェクトの場合、このプロパティは値の取得および設定が可能です。

**Required** プロパティを使用できるかどうかは、次の表に示すように、 **[Fields](fields-collection-dao.md)** コレクションを含むオブジェクトによって決まります。

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


**AllowZeroLength**、 **ValidateOnSet**、または **ValidationRule** の各プロパティに **Required** プロパティを使用すると、その **Field2** オブジェクトの **Value** プロパティの設定値の妥当性を調べることができます。 **Required** プロパティが **False** に設定されている場合、フィールドには **null** 値、および **AllowZeroLength** プロパティと **ValidationRule** プロパティの設定値で指定された条件を満たす値を含めることができます。


> [!NOTE]
> <P>[!メモ] <STRONG>Index</STRONG> オブジェクトと <STRONG>Field2</STRONG> オブジェクトのいずれかにこのプロパティを設定できる場合、 <STRONG>Field2</STRONG> オブジェクトのプロパティを設定します。 <STRONG>Field2</STRONG> オブジェクトのプロパティ設定の妥当性は、 <STRONG>Index</STRONG> オブジェクトのプロパティ設定よりも前に確認されます。</P>



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
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

