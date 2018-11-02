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
ms.openlocfilehash: 068496332479d25dfc4f20bdc683330ee462ce78
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927670"
---
# <a name="union-operation-microsoft-access-sql"></a>UNION 操作 (Microsoft Access SQL)


**適用されます**Access 2013、Office 2013。

ユニオン クエリを作成します。ユニオン クエリとは、独立した複数のクエリまたはテーブルの結果を結合するクエリのことです。

## <a name="syntax"></a>構文

\[テーブル\] *"クエリ 1"* UNION\[すべて\]\[テーブル\] *query2* \[和\[すべて\]\[テーブル\] *queryn* \[ . \]\]

UNION 操作には、次の指定項目があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>指定項目</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>query1-n</em></p></td>
<td><p>SELECT ステートメント、保存されたクエリ名、または TABLE に続けて指定する保存されたテーブル名。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

1 回の UNION 操作で、複数のクエリ、テーブル、および SELECT ステートメントの結果を、任意の組み合わせで結合することができます。次の例では、"New Accounts" という既存のテーブルと SELECT ステートメントを結合します。

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

UNION 操作を使用する場合、特に指定しなければ重複したレコードは返されません。ただし、[ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)) 述語を使用すると重複分を含むすべてのレコードが必ず返され、クエリの実行速度も速くなります。

UNION 操作でクエリが要求するフィールドの数は、すべてのクエリで同じである必要があります。ただし、フィールドのサイズやデータ型は同じである必要はありません。

別名は、先頭の SELECT ステートメントでのみ使用してください。これ以外の場所では無視されます。ORDER BY 句の中では、先頭の SELECT 句で使用しているフィールド名を使用してください。


> [!NOTE]
> <UL>
> <LI>
> <P>各<EM>クエリ</EM>の引数で、 <A href="https://msdn.microsoft.com/library/ff837271(v=office.15)">GROUP BY</A>句または<A href="https://msdn.microsoft.com/library/ff193795(v=office.15)">HAVING</A>句を使用すると、返されたデータをグループ化します。</P>
> <LI>
> <P><EM>クエリ</EM>の最後の引数の最後に指定された順序で返されるデータを表示するのには<A href="https://msdn.microsoft.com/library/ff198293(v=office.15)">ORDER BY</A>句を使用できます。</P></LI></UL>



## <a name="example"></a>例

次の使用例では、ブラジル国内のすべての仕入先および得意先の名前と都市名を取得します。

この例では、EnumFields プロシージャを呼び出します。EnumFields プロシージャについては、SELECT ステートメントの使用例を参照してください。

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
