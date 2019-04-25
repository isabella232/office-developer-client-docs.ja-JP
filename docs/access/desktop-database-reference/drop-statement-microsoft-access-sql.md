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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293652"
---
# <a name="drop-statement-microsoft-access-sql"></a><span data-ttu-id="7b07d-102">DROP ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="7b07d-102">DROP Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="7b07d-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7b07d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7b07d-104">データベースから既存のテーブル、プロシージャ、またはビューを削除するか、テーブルから既存のインデックスを削除します。</span><span class="sxs-lookup"><span data-stu-id="7b07d-104">Deletes an existing table, procedure, or view from a database, or deletes an existing index from a table.</span></span>

> [!NOTE]
> <span data-ttu-id="7b07d-p101">[!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは DROP 句や DDL (データ定義言語) ステートメントを使用できません。Microsoft Access データベース エンジン以外のデータベースでは、代わりに DAO の **Delete** 系メソッドを使用してください。</span><span class="sxs-lookup"><span data-stu-id="7b07d-p101">The Microsoft Access database engine does not support the use of DROP, or any of the DDL statements, with non-Microsoft Access database engine databases. Use the DAO **Delete** method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b07d-107">構文</span><span class="sxs-lookup"><span data-stu-id="7b07d-107">Syntax</span></span>

<span data-ttu-id="7b07d-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span><span class="sxs-lookup"><span data-stu-id="7b07d-108">DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}</span></span>

<span data-ttu-id="7b07d-109">DROP ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="7b07d-109">The DROP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b07d-110">パーツ</span><span class="sxs-lookup"><span data-stu-id="7b07d-110">Part</span></span></p></th>
<th><p><span data-ttu-id="7b07d-111">説明</span><span class="sxs-lookup"><span data-stu-id="7b07d-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b07d-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="7b07d-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="7b07d-113">削除されるテーブル、またはインデックスが削除されるテーブルの名前です。</span><span class="sxs-lookup"><span data-stu-id="7b07d-113">The name of the table to be deleted or the table from which an index is to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b07d-114"><em>procedure</em></span><span class="sxs-lookup"><span data-stu-id="7b07d-114"><em>procedure</em></span></span></p></td>
<td><p><span data-ttu-id="7b07d-115">削除されるプロシージャの名前です。</span><span class="sxs-lookup"><span data-stu-id="7b07d-115">The name of the procedure to be deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b07d-116"><em>view</em></span><span class="sxs-lookup"><span data-stu-id="7b07d-116"><em>view</em></span></span></p></td>
<td><p><span data-ttu-id="7b07d-117">削除されるビューの名前です。</span><span class="sxs-lookup"><span data-stu-id="7b07d-117">The name of the view to be deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b07d-118"><em>index</em></span><span class="sxs-lookup"><span data-stu-id="7b07d-118"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="7b07d-119">
            <em>テーブル</em>から削除されるインデックスの名前です。</span><span class="sxs-lookup"><span data-stu-id="7b07d-119">The name of the index to be deleted from <em>table.</em></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7b07d-120">注釈</span><span class="sxs-lookup"><span data-stu-id="7b07d-120">Remarks</span></span>

<span data-ttu-id="7b07d-121">テーブルを削除したり、テーブルからインデックスを削除したりするには、テーブルを閉じる必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b07d-121">You must close the table before you can delete it or remove an index from it.</span></span>

<span data-ttu-id="7b07d-122">[ALTER TABLE](alter-table-statement-microsoft-access-sql.md) ステートメントを使用してもテーブルからインデックスを削除できます。</span><span class="sxs-lookup"><span data-stu-id="7b07d-122">You can also use [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) to delete an index from a table.</span></span>

<span data-ttu-id="7b07d-p102">[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントを使用すると、テーブルを作成できます。 [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントまたは ALTER TABLE ステートメントを使用すると、インデックスを作成できます。テーブルを変更するには、ALTER TABLE ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7b07d-p102">You can use [CREATE TABLE](create-table-statement-microsoft-access-sql.md) to create a table and [CREATE INDEX](create-index-statement-microsoft-access-sql.md) or ALTER TABLE to create an index. To modify a table, use ALTER TABLE.</span></span>

## <a name="example"></a><span data-ttu-id="7b07d-125">例</span><span class="sxs-lookup"><span data-stu-id="7b07d-125">Example</span></span>

<span data-ttu-id="7b07d-126">次の使用例では、Northwind データベースの Employees テーブルに架空の NewIndex インデックスが存在していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="7b07d-126">The following example assumes the existence of a hypothetical NewIndex index on the Employees table in the Northwind database.</span></span>

<span data-ttu-id="7b07d-127">次の使用例では、MyIndex インデックスを Employees テーブルから削除します。</span><span class="sxs-lookup"><span data-stu-id="7b07d-127">This example deletes the index MyIndex from the Employees table.</span></span>

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

<span data-ttu-id="7b07d-128">次の使用例では、Employees テーブルをデータベースから削除します。</span><span class="sxs-lookup"><span data-stu-id="7b07d-128">This example deletes the Employees table from the database.</span></span>

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
