---
title: TableDef index メソッド (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: baa82b659cc2260d4a003c644b2d03d6c897fd21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314372"
---
# <a name="tabledefcreateindex-method-dao"></a>TableDef index メソッド (DAO)

**適用先:** Access 2013、Office 2013 

新しい**[Index](index-object-dao.md)** オブジェクトを作成します (Microsoft access ワークスペースのみ)。 .

## <a name="syntax"></a>構文

*式*。createindex (***名前***)

*式***TableDef**オブジェクトを表す変数を取得します。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>新しい <strong>Index</strong> オブジェクトの一意の名前を表す文字列型 (<strong>String</strong>) の値。 有効な <strong>Index</strong> 名の詳細については、<strong>Name</strong> プロパティを参照してください。</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>戻り値

Index

## <a name="remarks"></a>注釈

**CreateIndex** メソッドを使用して、 **TableDef** オブジェクトの新しい **Index** オブジェクトを作成できます。 **createindex**を使用するときに省略可能な名前の部分を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、 **name**プロパティを設定またはリセットできます。 オブジェクトの追加後に **Name** プロパティを設定できるかどうかは、 **Indexes** コレクションを格納しているオブジェクトの種類によって決まります。 詳細については、 **Name** プロパティのトピックを参照してください。

name が既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。

コレクションから **Index** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。

## <a name="example"></a>例

次の使用例では、 **CreateIndex** メソッドを使用して 2 つの新しい **Index** オブジェクトを作成し、これを Employees という名前の **TableDef** オブジェクトの **Indexes** コレクションに追加します。次に、 **TableDef** オブジェクトの Indexes コレクション、新しい **Index** オブジェクトの **Fields** コレクション、および新しい **Index** オブジェクトの Properties コレクションを列挙します。このプロシージャを実行するには、CreateIndexOutput 関数が必要です。

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
