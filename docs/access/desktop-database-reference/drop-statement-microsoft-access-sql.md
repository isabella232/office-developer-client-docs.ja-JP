---
title: DROP ステートメント (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f31067c96c19804352ca74957e064f9338b49260
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718295"
---
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="2455d-102">DROP ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="2455d-102">DROP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="2455d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2455d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2455d-104">データベースから既存のテーブル、プロシージャ、またはビューを削除したり、テーブルから既存のインデックスを削除したりします。</span><span class="sxs-lookup"><span data-stu-id="2455d-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="2455d-p101">[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは DROP 句や DDL (データ定義言語) ステートメントを使用できません。Microsoft Access データベース エンジン以外のデータベースでは、代わりに DAO の **Delete** 系メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="2455d-p101">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="2455d-107">構文</span><span class="sxs-lookup"><span data-stu-id="2455d-107">Syntax</span></span>

<span data-ttu-id="2455d-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span><span class="sxs-lookup"><span data-stu-id="2455d-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="2455d-109">DROP ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="2455d-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2455d-110">指定項目</span><span class="sxs-lookup"><span data-stu-id="2455d-110">Part</span></span></p></th>
<th><p><span data-ttu-id="2455d-111">説明</span><span class="sxs-lookup"><span data-stu-id="2455d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2455d-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="2455d-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="2455d-113">削除するテーブルの名前、または削除するインデックスのあるテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="2455d-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2455d-114"><em>procedure</em></span><span class="sxs-lookup"><span data-stu-id="2455d-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="2455d-115">削除するプロシージャの名前。</span><span class="sxs-lookup"><span data-stu-id="2455d-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2455d-116"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="2455d-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="2455d-117">削除するビューの名前。</span><span class="sxs-lookup"><span data-stu-id="2455d-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2455d-118"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="2455d-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="2455d-119">引数 <em>table</em> から削除するインデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="2455d-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2455d-120">解説</span><span class="sxs-lookup"><span data-stu-id="2455d-120">Remarks</span></span>

<span data-ttu-id="2455d-121">テーブルやテーブルのインデックスを削除するには、テーブルを閉じておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="2455d-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="2455d-122">[ALTER TABLE](alter-table-statement-microsoft-access-sql.md) ステートメントを使用してもテーブルからインデックスを削除できます。</span><span class="sxs-lookup"><span data-stu-id="2455d-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="2455d-p102">[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントを使用すると、テーブルを作成できます。 [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントまたは ALTER TABLE ステートメントを使用すると、インデックスを作成できます。テーブルを変更するには、ALTER TABLE ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="2455d-p102">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index. To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="2455d-125">使用例</span><span class="sxs-lookup"><span data-stu-id="2455d-125">Example</span></span>

<span data-ttu-id="2455d-126">次の使用例では、Northwind データベースの Employees テーブルに架空の NewIndex インデックスが存在していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="2455d-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="2455d-127">次の使用例では、MyIndex インデックスを Employees テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="2455d-127">This example deletes the index MyIndex from the Employees table.</span></span>

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

<span data-ttu-id="2455d-128">次の使用例では、Employees テーブルをデータベースから削除します。</span><span class="sxs-lookup"><span data-stu-id="2455d-128">This example deletes the Employees table from the database.</span></span>

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
