---
title: UNION 操作 (Microsoft Access SQL)
TOCTitle: UNION operation (Microsoft Access SQL)
ms:assetid: a5139921-51e5-7d96-74e3-11c3fd5f7eaa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821131(v=office.15)
ms:contentKeyID: 48546826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277582
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: f842e662f2576d8aab5f3857877f45e380d3d3b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314701"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="be38d-102">UNION 操作 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="be38d-102">UNION Operation (Microsoft Access SQL)</span></span>

<span data-ttu-id="be38d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="be38d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be38d-104">ユニオン クエリを作成します。ユニオン クエリとは、独立した複数のクエリまたはテーブルの結果を結合するクエリのことです。</span><span class="sxs-lookup"><span data-stu-id="be38d-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="be38d-105">構文</span><span class="sxs-lookup"><span data-stu-id="be38d-105">Syntax</span></span>

<span data-ttu-id="be38d-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span><span class="sxs-lookup"><span data-stu-id="be38d-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="be38d-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="be38d-107"></span></span>

<span data-ttu-id="be38d-108">UNION 操作には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="be38d-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be38d-109">パーツ</span><span class="sxs-lookup"><span data-stu-id="be38d-109">Part</span></span></p></th>
<th><p><span data-ttu-id="be38d-110">説明</span><span class="sxs-lookup"><span data-stu-id="be38d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be38d-111"><em>query1-n</em></span><span class="sxs-lookup"><span data-stu-id="be38d-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="be38d-112">SELECT ステートメント、保存されたクエリ名、または TABLE に続けて指定する保存されたテーブル名。</span><span class="sxs-lookup"><span data-stu-id="be38d-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="be38d-113">注釈</span><span class="sxs-lookup"><span data-stu-id="be38d-113">Remarks</span></span>

<span data-ttu-id="be38d-p102">2 つ以上のクエリ、テーブル、SELECT ステートメントの結果を結合し、1 つの UNION 操作を作成できます。次の例は、「New Accounts」という名前の既存テーブルと SELECT ステートメントを結合したものです。</span><span class="sxs-lookup"><span data-stu-id="be38d-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="be38d-p103">UNION 操作を使用する場合、特に指定しなければ重複したレコードは返されません。ただし、[ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) 述語を使用すると重複分を含むすべてのレコードが必ず返され、クエリの実行速度も速くなります。</span><span class="sxs-lookup"><span data-stu-id="be38d-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="be38d-118">UNION 操作でクエリが要求するフィールドの数は、すべてのクエリで同じである必要があります。ただし、フィールドのサイズやデータ型は同じである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="be38d-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="be38d-p104">エイリアスは最初の SELECT ステートメントでのみ使用します。他のステートメントでは無視されます。ORDER BY 句では、最初の SELECT ステートメントで呼ばれている名前でフィールドが参照されます。</span><span class="sxs-lookup"><span data-stu-id="be38d-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>

> [!NOTE]
> - <span data-ttu-id="be38d-121">引数 *query* のそれぞれのクエリ中で [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) 句や [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) 句を使用すると、返されるデータをグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="be38d-121">You can use a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause in each *query* argument to group the returned data.</span></span>
> - <span data-ttu-id="be38d-122">引数 *query* の末尾に指定するクエリで [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) 句を使用すると、返されるデータを指定の順序で表示できます。</span><span class="sxs-lookup"><span data-stu-id="be38d-122">You can use an [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) clause at the end of the last *query* argument to display the returned data in a specified order.</span></span>

## <a name="example"></a><span data-ttu-id="be38d-123">例</span><span class="sxs-lookup"><span data-stu-id="be38d-123">Example</span></span>

<span data-ttu-id="be38d-124">次の使用例では、ブラジル国内のすべての仕入先および得意先の名前と都市名を取得します。</span><span class="sxs-lookup"><span data-stu-id="be38d-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="be38d-125">EnumFields プロシージャを呼び出しますが、このプロシージャについては、SELECT ステートメントの使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="be38d-125">This example calls the EnumFields procedure, which you can find in the SELECT statement example.

</span></span>

```vb
    Sub UnionX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Retrieve the names and cities of all suppliers  
        ' and customers in Brazil. 
        Set rst = dbs.OpenRecordset("SELECT CompanyName," _ 
            & " City FROM Suppliers" _ 
            & " WHERE Country = 'Brazil' UNION" _ 
            & " SELECT CompanyName, City FROM Customers" _ 
            & " WHERE Country = 'Brazil';") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 12 
     
        dbs.Close 
     
    End Sub
```
