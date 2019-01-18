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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716251"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="1f97f-102">UNION 操作 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1f97f-102">UNION operation (Microsoft Access SQL)</span></span>

<span data-ttu-id="1f97f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1f97f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1f97f-104">ユニオン クエリを作成します。ユニオン クエリとは、独立した複数のクエリまたはテーブルの結果を結合するクエリのことです。</span><span class="sxs-lookup"><span data-stu-id="1f97f-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f97f-105">構文</span><span class="sxs-lookup"><span data-stu-id="1f97f-105">Syntax</span></span>

<span data-ttu-id="1f97f-106">\[テーブル\] *"クエリ 1"* UNION\[すべて\]\[テーブル\] *query2* \[和\[すべて\]\[テーブル\] *queryn* \[ .</span><span class="sxs-lookup"><span data-stu-id="1f97f-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="1f97f-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="1f97f-107"></span></span>

<span data-ttu-id="1f97f-108">UNION 操作には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="1f97f-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f97f-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="1f97f-109">Part</span></span></p></th>
<th><p><span data-ttu-id="1f97f-110">説明</span><span class="sxs-lookup"><span data-stu-id="1f97f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f97f-111"><em>query1-n</em></span><span class="sxs-lookup"><span data-stu-id="1f97f-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="1f97f-112">SELECT ステートメント、保存されたクエリ名、または TABLE に続けて指定する保存されたテーブル名。</span><span class="sxs-lookup"><span data-stu-id="1f97f-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1f97f-113">解説</span><span class="sxs-lookup"><span data-stu-id="1f97f-113">Remarks</span></span>

<span data-ttu-id="1f97f-p102">1 回の UNION 操作で、複数のクエリ、テーブル、および SELECT ステートメントの結果を、任意の組み合わせで結合することができます。次の例では、"New Accounts" という既存のテーブルと SELECT ステートメントを結合します。</span><span class="sxs-lookup"><span data-stu-id="1f97f-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="1f97f-p103">UNION 操作を使用する場合、特に指定しなければ重複したレコードは返されません。ただし、[ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) 述語を使用すると重複分を含むすべてのレコードが必ず返され、クエリの実行速度も速くなります。</span><span class="sxs-lookup"><span data-stu-id="1f97f-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="1f97f-118">UNION 操作でクエリが要求するフィールドの数は、すべてのクエリで同じである必要があります。ただし、フィールドのサイズやデータ型は同じである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1f97f-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="1f97f-p104">別名は、先頭の SELECT ステートメントでのみ使用してください。これ以外の場所では無視されます。ORDER BY 句の中では、先頭の SELECT 句で使用しているフィールド名を使用してください。</span><span class="sxs-lookup"><span data-stu-id="1f97f-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>

> [!NOTE]
> - <span data-ttu-id="1f97f-121">各*クエリ*の引数で、 [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql)句または[HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql)句を使用すると、返されたデータをグループ化します。</span><span class="sxs-lookup"><span data-stu-id="1f97f-121">You can use a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause in each *query* argument to group the returned data.</span></span>
> - <span data-ttu-id="1f97f-122">*クエリ*の最後の引数の最後に指定された順序で返されるデータを表示するのには[ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql)句を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1f97f-122">You can use an [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) clause at the end of the last *query* argument to display the returned data in a specified order.</span></span>

## <a name="example"></a><span data-ttu-id="1f97f-123">例</span><span class="sxs-lookup"><span data-stu-id="1f97f-123">Example</span></span>

<span data-ttu-id="1f97f-124">次の使用例では、ブラジル国内のすべての仕入先および得意先の名前と都市名を取得します。</span><span class="sxs-lookup"><span data-stu-id="1f97f-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span> <span data-ttu-id="1f97f-125">SELECT ステートメントの例で表示できる、EnumFields プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1f97f-125">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
