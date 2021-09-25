---
title: Index.DistinctCount プロパティ (DAO)
TOCTitle: DistinctCount Property
ms:assetid: 24cb7247-76b4-1fce-c3c4-892f16634eff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191836(v=office.15)
ms:contentKeyID: 48543767
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053119
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 50a649478a117e79e3cf931976f2520a107ac38d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606626"
---
# <a name="indexdistinctcount-property-dao"></a>Index.DistinctCount プロパティ (DAO)

**適用先**: Access 2013、Office 2013

関連付けられたテーブルに含まれる **[Index](index-object-dao.md)** オブジェクトの一意の値の数を示す値を返します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式* .DistinctCount

*式* Index オブジェクトを表す **変数** 。

## <a name="remarks"></a>注釈

インデックスの一意の値または一意のキーの数を確認するには、 **DistinctCount** プロパティを確認します。インデックスに重複値が許可されていると、その値が複数個存在する場合もありますが、キーをカウントするのは 1 回のみです。この情報は、インデックス情報を評価することでデータ アクセスを最適化しようとするアプリケーションで役立ちます。一意の値の数は、 **Index** オブジェクトのカーディナリティとも呼ばれます。

**DistinctCount** プロパティは、特定の時点の実際のキー数を常に反映するわけではありません。たとえば、ロールバックされたトランザクションによって発生する変更は、 **DistinctCount** プロパティには直ちに反映されません。一意のキーを持つレコードの削除も、 **DistinctCount** プロパティの値に反映されない場合があります。 **[CreateIndex](tabledef-createindex-method-dao.md)** メソッドを使用した直後は、数値が正確になります。

## <a name="example"></a>例

次の使用例は、 **DistinctCount** プロパティを使用して、 **Index** オブジェクトの一意の値の数を調べる方法を示します。ただし、この値が正確なのは、 **Index** オブジェクトを作成した直後のみです。キーの変更、つまり新しいキーの追加や古いキーの削除がない場合は、値は正確なままですが、それ以外の場合は不正確な可能性があります (このプロシージャを複数回実行する場合、既存の Index オブジェクトの **DistinctCount** プロパティの値で結果を確認できます)。

```vb
    Sub DistinctCountX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxLoop As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create and append new Index object to the Employees 
     ' table. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     idxCountry.Fields.Append _ 
     idxCountry.CreateField("Country") 
     .Indexes.Append idxCountry 
     
     ' The collection must be refreshed for the new 
     ' DistinctCount data to be available. 
     .Indexes.Refresh 
     
     ' Enumerate Indexes collection to show the current 
     ' DistinctCount values. 
     Debug.Print "Indexes before adding new record" 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Add a new record to the Employees table. 
     With rstEmployees 
     .AddNew 
     !FirstName = "April" 
     !LastName = "LaMonte" 
     !Country = "Canada" 
     .Update 
     End With 
     
     ' Enumerate Indexes collection to show the modified 
     ' DistinctCount values. 
     Debug.Print "Indexes after adding new record and " & _ 
     "refreshing Indexes" 
     .Indexes.Refresh 
     For Each idxLoop In .Indexes 
     Debug.Print " DistinctCount = " & _ 
     idxLoop.DistinctCount & ", Name = " & _ 
     idxLoop.Name 
     Next idxLoop 
     
     ' Delete new record because this is a demonstration. 
     With rstEmployees 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Indexes because this is a demonstration. 
     .Indexes.Delete idxCountry.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
