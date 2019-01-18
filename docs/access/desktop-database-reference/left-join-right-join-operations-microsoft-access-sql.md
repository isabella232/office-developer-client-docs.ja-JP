---
title: LEFT JOIN、RIGHT JOIN 操作 (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: c6e37cd68d586e39a06fd650ccb453f35477253f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704722"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="d0666-102">LEFT JOIN、RIGHT JOIN 操作 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="d0666-102">LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="d0666-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d0666-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d0666-104">[FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句の中で使用され、ソース テーブルのレコードを結合します。</span><span class="sxs-lookup"><span data-stu-id="d0666-104">Combines source-table records when used in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0666-105">構文</span><span class="sxs-lookup"><span data-stu-id="d0666-105">Syntax</span></span>

<span data-ttu-id="d0666-106">*Table1 という名前*の\[左 |右\] *table1.field1* *compopr table2.field2*では、結合*テーブル 2*</span><span class="sxs-lookup"><span data-stu-id="d0666-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span></span>

<span data-ttu-id="d0666-107">LEFT JOIN 操作および RIGHT JOIN 操作には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="d0666-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d0666-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="d0666-108">Part</span></span></p></th>
<th><p><span data-ttu-id="d0666-109">説明</span><span class="sxs-lookup"><span data-stu-id="d0666-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d0666-110"><em>table1</em>、<em>table2</em></span><span class="sxs-lookup"><span data-stu-id="d0666-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="d0666-111">結合するレコードのあるテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="d0666-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d0666-112"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="d0666-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="d0666-p101">結合するフィールドの名前。両方のフィールドが同じデータ型で、格納されるデータが同じ種類である必要があります。ただし、同じ名前である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d0666-p101">The names of the fields that are joined. The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d0666-115"><em>compopr</em></span><span class="sxs-lookup"><span data-stu-id="d0666-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="d0666-116">任意の関係比較演算子: &quot;=&quot; &quot; &lt;、&quot; &quot; &gt;、&quot; &quot; &lt;=&quot; &quot; &gt;=、&quot;または&quot; &lt; &gt;。&quot;</span><span class="sxs-lookup"><span data-stu-id="d0666-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d0666-117">解説</span><span class="sxs-lookup"><span data-stu-id="d0666-117">Remarks</span></span>

<span data-ttu-id="d0666-p102">左外部結合を作成するには、LEFT JOIN 操作を使用します。左外部結合では、結合する 2 つのテーブルのうち 2 番目 (右側) のテーブルに対応するレコードがなくても、1 番目 (左側) のテーブルのレコードがすべて追加されます。</span><span class="sxs-lookup"><span data-stu-id="d0666-p102">Use a LEFT JOIN operation to create a left outer join. Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="d0666-p103">右外部結合を作成するには、RIGHT JOIN 操作を使用します。右外部結合では、結合する 2 つのテーブルのうち 1 番目 (左側) のテーブルに対応するレコードがなくても、2 番目 (右側) のテーブルのレコードがすべて追加されます。</span><span class="sxs-lookup"><span data-stu-id="d0666-p103">Use a RIGHT JOIN operation to create a right outer join. Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="d0666-p104">たとえば、[部署] テーブル (左側) と [社員] テーブル (右側) がある場合に、どの部署にも所属しない社員も含めた全社員を選択するには、RIGHT JOIN 操作を使用します。反対に、社員が配属されていない部署も含めたすべての部署を選択するには、LEFT JOIN 操作を使用します。</span><span class="sxs-lookup"><span data-stu-id="d0666-p104">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them. To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="d0666-p105">次の例では、Categories テーブルと Products テーブルを CategoryID フィールドで結合しています。このクエリでは、商品がまったくない商品区分も含めて、すべての商品区分の一覧が出力されます。</span><span class="sxs-lookup"><span data-stu-id="d0666-p105">The following example shows how you could join the Categories and Products tables on the CategoryID field. The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="d0666-126">この例では、[区分コード] は、結合されたフィールドですが、 [SELECT](select-statement-microsoft-access-sql.md)ステートメントに含まれていないために、クエリの結果には含まれません。</span><span class="sxs-lookup"><span data-stu-id="d0666-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="d0666-127">結合フィールドを含むように、SELECT ステートメントでフィールド名を入力します: ここで指定してください。</span><span class="sxs-lookup"><span data-stu-id="d0666-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="d0666-128">結合フィールドのデータが同じレコードのみを選択するクエリを作成するには、[INNER JOIN](inner-join-operation-microsoft-access-sql.md) 操作を使用します。</span><span class="sxs-lookup"><span data-stu-id="d0666-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="d0666-p107">LEFT JOIN および RIGHT JOIN は、INNER JOIN の中にネストすることができます。しかし、INNER JOIN を LEFT JOIN または RIGHT JOIN の中にネストすることはできません。結合を他の結合にネストする方法の詳細については、「INNER JOIN 操作」のネストに関する説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0666-p107">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN. See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="d0666-p108">ON 句は複数連結できます。詳細については、「INNER JOIN 操作」の連結に関する説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0666-p108">You can link multiple ON clauses. See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="d0666-133">メモ型 (Memo) または OLE オブジェクト型 (OLE Object) のデータが格納されたフィールドを結合しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d0666-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="d0666-134">例</span><span class="sxs-lookup"><span data-stu-id="d0666-134">Example</span></span>

<span data-ttu-id="d0666-135">この例では:</span><span class="sxs-lookup"><span data-stu-id="d0666-135">This example:</span></span>
- <span data-ttu-id="d0666-136">[社員] テーブルには、架空の部署名、部署 ID フィールドの存在を前提としています。</span><span class="sxs-lookup"><span data-stu-id="d0666-136">Assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="d0666-137">これらのフィールドは存在しないこと実際には Northwind データベースの Employees テーブルに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d0666-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="d0666-138">従業員も含め、すべての部門を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0666-138">Selects all departments, including those without employees.</span></span>

- <span data-ttu-id="d0666-139">SELECT ステートメントの例である EnumFields プロシージャを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d0666-139">Calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
