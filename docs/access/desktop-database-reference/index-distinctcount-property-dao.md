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
ms.openlocfilehash: 2e609090e66a9bfd5b4b37d8e8e8a5546cc8469a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876891"
---
# <a name="indexdistinctcount-property-dao"></a><span data-ttu-id="863cb-102">Index.DistinctCount プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="863cb-102">Index.DistinctCount Property (DAO)</span></span>

<span data-ttu-id="863cb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="863cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="863cb-104">関連付けられたテーブルに含まれる **[Index](index-object-dao.md)** オブジェクトの一意の値の数を示す値を返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="863cb-104">Returns a value that indicates the number of unique values for the **[Index](index-object-dao.md)** object that are included in the associated table (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="863cb-105">構文</span><span class="sxs-lookup"><span data-stu-id="863cb-105">Syntax</span></span>

<span data-ttu-id="863cb-106">*式*です。DistinctCount</span><span class="sxs-lookup"><span data-stu-id="863cb-106">*expression* .DistinctCount</span></span>

<span data-ttu-id="863cb-107">\*式\***Index**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="863cb-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="863cb-108">注釈</span><span class="sxs-lookup"><span data-stu-id="863cb-108">Remarks</span></span>

<span data-ttu-id="863cb-p101">インデックスの一意の値または一意のキーの数を確認するには、 **DistinctCount** プロパティを確認します。インデックスに重複値が許可されていると、その値が複数個存在する場合もありますが、キーをカウントするのは 1 回のみです。この情報は、インデックス情報を評価することでデータ アクセスを最適化しようとするアプリケーションで役立ちます。一意の値の数は、 **Index** オブジェクトのカーディナリティとも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="863cb-p101">Check the **DistinctCount** property to determine the number of unique values, or keys, in an index. Any key is counted only once, even though there may be multiple occurrences of that value if the index permits duplicate values. This information is useful in applications that attempt to optimize data access by evaluating index information. The number of unique values is also known as the cardinality of an **Index** object.</span></span>

<span data-ttu-id="863cb-p102">**DistinctCount** プロパティは、特定の時点の実際のキー数を常に反映するわけではありません。たとえば、ロールバックされたトランザクションによって発生する変更は、 **DistinctCount** プロパティには直ちに反映されません。一意のキーを持つレコードの削除も、 **DistinctCount** プロパティの値に反映されない場合があります。 **[CreateIndex](tabledef-createindex-method-dao.md)** メソッドを使用した直後は、数値が正確になります。</span><span class="sxs-lookup"><span data-stu-id="863cb-p102">The **DistinctCount** property won't always reflect the actual number of keys at a particular time. For example, a change caused by a rolled back transaction won't be reflected immediately in the **DistinctCount** property. The **DistinctCount** property value also may not reflect the deletion of records with unique keys. The number will be accurate immediately after you use the **[CreateIndex](tabledef-createindex-method-dao.md)** method.</span></span>

## <a name="example"></a><span data-ttu-id="863cb-117">例</span><span class="sxs-lookup"><span data-stu-id="863cb-117">Example</span></span>

<span data-ttu-id="863cb-p103">次の使用例は、 **DistinctCount** プロパティを使用して、 **Index** オブジェクトの一意の値の数を調べる方法を示します。ただし、この値が正確なのは、 **Index** オブジェクトを作成した直後のみです。キーの変更、つまり新しいキーの追加や古いキーの削除がない場合は、値は正確なままですが、それ以外の場合は不正確な可能性があります (このプロシージャを複数回実行する場合、既存の Index オブジェクトの **DistinctCount** プロパティの値で結果を確認できます)。</span><span class="sxs-lookup"><span data-stu-id="863cb-p103">This example uses the **DistinctCount** property to show how you can determine the number of unique values in an **Index** object. However, this value is only accurate immediately after creating the **Index**. It will remain accurate if no keys change, or if new keys are added and no old keys are deleted; otherwise, it will not be reliable. (If this procedure is run several times, you can see the effect on the **DistinctCount** property values of the existing Index objects.)</span></span>

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
