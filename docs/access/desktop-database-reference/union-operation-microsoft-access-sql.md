---
title: UNION 操作 (Microsoft Access SQL)
TOCTitle: UNION Operation (Microsoft Access SQL)
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
ms.openlocfilehash: 9a06a5598716bb57d05048d861fcb13b1813365f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477513"
---
# <a name="union-operation-microsoft-access-sql"></a><span data-ttu-id="6318f-102">UNION 操作 (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="6318f-102">UNION Operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="6318f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6318f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6318f-104">ユニオン クエリを作成します。ユニオン クエリとは、独立した複数のクエリまたはテーブルの結果を結合するクエリのことです。</span><span class="sxs-lookup"><span data-stu-id="6318f-104">Creates a union query, which combines the results of two or more independent queries or tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="6318f-105">構文</span><span class="sxs-lookup"><span data-stu-id="6318f-105">Syntax</span></span>

<span data-ttu-id="6318f-106">\[テーブル\] *"クエリ 1"* UNION\[すべて\]\[テーブル\] *query2* \[和\[すべて\]\[テーブル\] *queryn* \[ .</span><span class="sxs-lookup"><span data-stu-id="6318f-106">\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ …</span></span> <span data-ttu-id="6318f-107">\]\]</span><span class="sxs-lookup"><span data-stu-id="6318f-107"></span></span>

<span data-ttu-id="6318f-108">UNION 操作には、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="6318f-108">The UNION operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6318f-109">指定項目</span><span class="sxs-lookup"><span data-stu-id="6318f-109">Part</span></span></p></th>
<th><p><span data-ttu-id="6318f-110">説明</span><span class="sxs-lookup"><span data-stu-id="6318f-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6318f-111"><em>query1-n</em></span><span class="sxs-lookup"><span data-stu-id="6318f-111"><em>query1-n</em></span></span></p></td>
<td><p><span data-ttu-id="6318f-112">SELECT ステートメント、保存されたクエリ名、または TABLE に続けて指定する保存されたテーブル名。</span><span class="sxs-lookup"><span data-stu-id="6318f-112">A SELECT statement, the name of a stored query, or the name of a stored table preceded by the TABLE keyword.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6318f-113">解説</span><span class="sxs-lookup"><span data-stu-id="6318f-113">Remarks</span></span>

<span data-ttu-id="6318f-p102">1 回の UNION 操作で、複数のクエリ、テーブル、および SELECT ステートメントの結果を、任意の組み合わせで結合することができます。次の例では、"New Accounts" という既存のテーブルと SELECT ステートメントを結合します。</span><span class="sxs-lookup"><span data-stu-id="6318f-p102">You can merge the results of two or more queries, tables, and SELECT statements, in any combination, in a single UNION operation. The following example merges an existing table named New Accounts and a SELECT statement:</span></span>

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

<span data-ttu-id="6318f-p103">UNION 操作を使用する場合、特に指定しなければ重複したレコードは返されません。ただし、[ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) 述語を使用すると重複分を含むすべてのレコードが必ず返され、クエリの実行速度も速くなります。</span><span class="sxs-lookup"><span data-stu-id="6318f-p103">By default, no duplicate records are returned when you use a UNION operation; however, you can include the [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) predicate to ensure that all records are returned. This also makes the query run faster.</span></span>

<span data-ttu-id="6318f-118">UNION 操作でクエリが要求するフィールドの数は、すべてのクエリで同じである必要があります。ただし、フィールドのサイズやデータ型は同じである必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6318f-118">All queries in a UNION operation must request the same number of fields; however, the fields do not have to be of the same size or data type.</span></span>

<span data-ttu-id="6318f-p104">別名は、先頭の SELECT ステートメントでのみ使用してください。これ以外の場所では無視されます。ORDER BY 句の中では、先頭の SELECT 句で使用しているフィールド名を使用してください。</span><span class="sxs-lookup"><span data-stu-id="6318f-p104">Use aliases only in the first SELECT statement because they are ignored in any others. In the ORDER BY clause, refer to fields by what they are called in the first SELECT statement.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="6318f-121">各<EM>クエリ</EM>の引数で、 <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A>句または<A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A>句を使用すると、返されたデータをグループ化します。</span><span class="sxs-lookup"><span data-stu-id="6318f-121">You can use a <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A> or <A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A> clause in each <EM>query</EM> argument to group the returned data.</span></span></P>
> <LI>
> <P><span data-ttu-id="6318f-122"><EM>クエリ</EM>の最後の引数の最後に指定された順序で返されるデータを表示するのには<A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A>句を使用できます。</span><span class="sxs-lookup"><span data-stu-id="6318f-122">You can use an <A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A> clause at the end of the last <EM>query</EM> argument to display the returned data in a specified order.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="6318f-123">例</span><span class="sxs-lookup"><span data-stu-id="6318f-123">Example</span></span>

<span data-ttu-id="6318f-124">次の使用例では、ブラジル国内のすべての仕入先および得意先の名前と都市名を取得します。</span><span class="sxs-lookup"><span data-stu-id="6318f-124">This example retrieves the names and cities of all suppliers and customers in Brazil.</span></span>

<span data-ttu-id="6318f-125">この例では、EnumFields プロシージャを呼び出します。EnumFields プロシージャについては、SELECT ステートメントの使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6318f-125">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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