---
title: INNER JOIN 操作 (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e4179087408a9f7a68bccc673bcd456305ba41d5
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026485"
---
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="b17f2-102">INNER JOIN 操作 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b17f2-102">INNER JOIN operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="b17f2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b17f2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b17f2-104">2 つのテーブルの共通するフィールドに同じ値があった場合に、両方のテーブルのレコードを結合します。</span><span class="sxs-lookup"><span data-stu-id="b17f2-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="b17f2-105">構文</span><span class="sxs-lookup"><span data-stu-id="b17f2-105">Syntax</span></span>

<span data-ttu-id="b17f2-106">*Table1 という名前*の内部結合*table2*から*table1 という名前*にします。*フィールド 1\*\*table2 を compopr*。*フィールド 2*</span><span class="sxs-lookup"><span data-stu-id="b17f2-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span></span>

<span data-ttu-id="b17f2-107">INNER JOIN 操作には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="b17f2-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b17f2-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="b17f2-108">Part</span></span></p></th>
<th><p><span data-ttu-id="b17f2-109">説明</span><span class="sxs-lookup"><span data-stu-id="b17f2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b17f2-110"><em>table1</em>、<em>table2</em></span><span class="sxs-lookup"><span data-stu-id="b17f2-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="b17f2-111">結合するレコードのあるテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="b17f2-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b17f2-112"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="b17f2-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="b17f2-p101">結合するフィールドの名前。フィールドが数値型 (Numeric) でない場合は、両方のフィールドが同じデータ型であり、両方のフィールドに格納されているデータが同じ種類である必要があります。ただし、同じ名前である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b17f2-p101">The names of the fields that are joined. If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b17f2-115"><em>compopr</em></span><span class="sxs-lookup"><span data-stu-id="b17f2-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="b17f2-116">任意の関係比較演算子: &quot;=&quot; &quot; &lt;、&quot; &quot; &gt;、&quot; &quot; &lt;=&quot; &quot; &gt;=、&quot;または&quot; &lt; &gt;。&quot;</span><span class="sxs-lookup"><span data-stu-id="b17f2-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b17f2-117">解説</span><span class="sxs-lookup"><span data-stu-id="b17f2-117">Remarks</span></span>

<span data-ttu-id="b17f2-p102">INNER JOIN 操作は、[FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句の中で使用します。INNER JOIN 操作は最も一般的な結合方法です。2 つのテーブルの共通するフィールドに同じ種類の値があった場合に、両方のテーブルのレコードを結合します。</span><span class="sxs-lookup"><span data-stu-id="b17f2-p102">You can use an INNER JOIN operation in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause. This is the most common type of join. Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="b17f2-p103">たとえば、[部署] テーブルと [社員] テーブルで INNER JOIN 操作を行うと、各部署に所属する社員全員を選択できます。これに対して、所属する社員が 1 人もいない部署も含めすべての部署を選択したり、どの部署にも所属していない社員も含め社員全員を選択したりするには、[LEFT JOIN または RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) 操作を使用して外部結合を作成します。</span><span class="sxs-lookup"><span data-stu-id="b17f2-p103">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="b17f2-123">メモ型 (Memo) または OLE オブジェクト型 (OLE Object) のデータが格納されたフィールドを結合しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="b17f2-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="b17f2-p104">2 つの数値型 (Numeric) フィールドのデータ型が同じであれば、それらのフィールドを結合することができます。たとえば、オートナンバ型 (AutoNumber) フィールドと長整数型 (Long) フィールドは、データ型が同じであるため結合することができます。一方、単精度浮動小数点型 (Single) フィールドと倍精度浮動小数点型 (Double) フィールドは結合できません。</span><span class="sxs-lookup"><span data-stu-id="b17f2-p104">You can join any two numeric fields of like types. For example, you can join on AutoNumber and Long fields because they are like types. However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="b17f2-127">次の例では、Categories テーブルと Products テーブルを CategoryID フィールドで結合しています。</span><span class="sxs-lookup"><span data-stu-id="b17f2-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="b17f2-128">上記の例では、[区分コード] は、結合されたフィールドですが、 [SELECT](select-statement-microsoft-access-sql.md)ステートメントに含まれていないために、クエリ出力には含まれません。</span><span class="sxs-lookup"><span data-stu-id="b17f2-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="b17f2-129">結合フィールドを含めるには、そのフィールド名を SELECT ステートメントで、この例で指定してください。</span><span class="sxs-lookup"><span data-stu-id="b17f2-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="b17f2-130">次の構文を使用して、JOIN ステートメントの中で複数の ON 句を連結できます。</span><span class="sxs-lookup"><span data-stu-id="b17f2-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="b17f2-131">*フィールド*FROM *table1* INNER JOIN *table2*に*table1 という名前*を選択します。*フィールド 1**compopr**table2*。*フィールド 1\*\*Table1 という名前*にします。*フィールド 2**compopr**table2*。*field2*)*Table1 という名前*にします。*field3**compopr**table2*。*field3*)\];</span><span class="sxs-lookup"><span data-stu-id="b17f2-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND ON *table1*.*field2* *compopr* *table2*.*field2*) OR ON *table1*.*field3* *compopr* *table2*.*field3*)\];</span></span>

<span data-ttu-id="b17f2-132">次の構文を使用して、JOIN ステートメントをネストすることができます。</span><span class="sxs-lookup"><span data-stu-id="b17f2-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="b17f2-133">INNER JOIN*フィールド*FROM *table1 という名前*を選択 (*table2*の INNER JOIN \[( \]*テーブル 3* \[INNER JOIN \[( \] *tablex* \[内部に参加しています)\] *テーブル 3*にします。*field3**compopr**tablex*。*fieldx*)\] *テーブル 2*にします。*フィールド 2**compopr**テーブル 3*です。*field3*)*Table1 という名前*にします。*フィールド 1**compopr**table2*。*フィールド 2*です。</span><span class="sxs-lookup"><span data-stu-id="b17f2-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span></span>

<span data-ttu-id="b17f2-134">LEFT JOIN または RIGHT JOIN は、INNER JOIN にネストできますが、INNER JOIN を LEFT JOIN または RIGHT JOIN にネストすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b17f2-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="b17f2-135">使用例</span><span class="sxs-lookup"><span data-stu-id="b17f2-135">Example</span></span>

<span data-ttu-id="b17f2-p106">次の使用例では、Order Details テーブルと Orders テーブルの等結合、および Orders テーブルと Employees テーブルの等結合を作成します。この結合が必要になるのは、Employees テーブルに売上データが含まれず、Order Details テーブルに社員データが含まれないためです。クエリによって、社員名と、その社員の総売上高の一覧が生成されます。</span><span class="sxs-lookup"><span data-stu-id="b17f2-p106">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="b17f2-139">この例では、EnumFields プロシージャを呼び出します。EnumFields プロシージャについては、SELECT ステートメントの使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b17f2-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
