---
title: DELETE ステートメント (Microsoft Access SQL)
TOCTitle: DELETE Statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d8a0d78350a9689af67f33262ff510d8638de40c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477952"
---
# <a name="delete-statement-microsoft-access-sql"></a><span data-ttu-id="45c81-102">DELETE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="45c81-102">DELETE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="45c81-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="45c81-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="45c81-104">[FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) 句で指定したテーブルから [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) 句の条件を満たすレコードを削除する削除クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="45c81-104">Creates a delete query that removes records from one or more of the tables listed in the [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause that satisfy the [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="45c81-105">構文</span><span class="sxs-lookup"><span data-stu-id="45c81-105">Syntax</span></span>

<span data-ttu-id="45c81-106">削除\[*テーブル*です。\* \] *テーブル*から、*抽出条件*</span><span class="sxs-lookup"><span data-stu-id="45c81-106">DELETE \[*table*.\*\] FROM *table* WHERE *criteria*</span></span>

<span data-ttu-id="45c81-107">DELETE ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="45c81-107">The DELETE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="45c81-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="45c81-108">Part</span></span></p></th>
<th><p><span data-ttu-id="45c81-109">説明</span><span class="sxs-lookup"><span data-stu-id="45c81-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="45c81-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="45c81-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="45c81-111">削除するレコードのあるテーブルの名前。この項目は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="45c81-111">The optional name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="45c81-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="45c81-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="45c81-113">削除するレコードのあるテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="45c81-113">The name of the table from which records are deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="45c81-114"><em>criteria</em></span><span class="sxs-lookup"><span data-stu-id="45c81-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="45c81-115">削除するレコードを決める式。</span><span class="sxs-lookup"><span data-stu-id="45c81-115">An expression that determines which records to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="45c81-116">解説</span><span class="sxs-lookup"><span data-stu-id="45c81-116">Remarks</span></span>

<span data-ttu-id="45c81-117">DELETE ステートメントは、多数のレコードを削除する場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="45c81-117">DELETE is especially useful when you want to delete many records.</span></span>

<span data-ttu-id="45c81-p101">データベースからあるテーブル全体を削除するには、**DROP** ステートメントで [Execute](drop-statement-microsoft-access-sql.md) メソッドを使用します。ただし、テーブルを削除するとテーブルの構造も失われます。これに対して、DELETE ステートメントを使用した場合はデータのみが削除され、テーブルの構造や、フィールド属性、インデックスなどのテーブル プロパティはすべてそのまま残されます。</span><span class="sxs-lookup"><span data-stu-id="45c81-p101">To drop an entire table from the database, you can use the **Execute** method with a [DROP](drop-statement-microsoft-access-sql.md) statement. If you delete the table, however, the structure is lost. In contrast, when you use DELETE, only the data is deleted; the table structure and all of the table properties, such as field attributes and indexes, remain intact.</span></span>

<span data-ttu-id="45c81-p102">DELETE ステートメントを使用すると、あるテーブルとの間に一対多リレーションシップがある複数のテーブルからレコードを削除できます。連鎖削除を行うと、"一" 側のテーブルに含まれるレコードがクエリで削除された場合に、"多" 側にある対応するレコードも削除されます。たとえば、[得意先] テーブルと [注文] テーブルとの間にリレーションシップが設定されていて、[得意先] テーブルが "一" 側、[注文] テーブルが "多" 側であるとします。この場合、連鎖削除オプションが指定されていれば、[得意先] テーブルからレコードを削除すると、それに対応する [注文] テーブルのレコードも削除されます。</span><span class="sxs-lookup"><span data-stu-id="45c81-p102">You can use DELETE to remove records from tables that are in a one-to-many relationship with other tables. Cascade delete operations cause the records in tables that are on the many side of the relationship to be deleted when the corresponding record in the one side of the relationship is deleted in the query. For example, in the relationship between the Customers and Orders tables, the Customers table is on the one side and the Orders table is on the many side of the relationship. Deleting a record from Customers results in the corresponding Orders records being deleted if the cascade delete option is specified.</span></span>

<span data-ttu-id="45c81-p103">削除クエリでは、レコード全体が削除されます。特定のフィールドのデータのみを削除することはできません。特定のフィールド値を削除する場合は、値を **Null** 値に変更する更新クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="45c81-p103">A delete query deletes entire records, not just data in specific fields. If you want to delete values in a specific field, create an update query that changes the values to **Null**.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="45c81-p104">特定のフィールド値を削除する場合は、値を Null 値に変更する更新クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="45c81-p104">After you remove records using a delete query, you cannot undo the operation. If you want to know which records were deleted, first examine the results of a select query that uses the same criteria, and then run the delete query.</span></span>
> - <span data-ttu-id="45c81-p105">削除クエリでいったん削除したレコードは、元に戻せません。</span><span class="sxs-lookup"><span data-stu-id="45c81-p105">Maintain backup copies of your data at all times. If you delete the wrong records, you can retrieve them from your backup copies.</span></span>

## <a name="example"></a><span data-ttu-id="45c81-131">使用例</span><span class="sxs-lookup"><span data-stu-id="45c81-131">Example</span></span>

<span data-ttu-id="45c81-p106">次の使用例では、役職が Trainee である社員のすべてのレコードを削除します。FROM 句に 1 つのテーブルのみが含まれている場合は、テーブル名を DELETE ステートメントにリストする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="45c81-p106">This example deletes all records for employees whose title is Trainee. When the FROM clause includes only one table, you do not have to list the table name in the DELETE statement.</span></span>

```vb
    Sub DeleteX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete employee records where title is Trainee.     
        dbs.Execute "DELETE * FROM " _ 
            & "Employees WHERE Title = 'Trainee';" 
         
        dbs.Close 
     
    End Sub
```