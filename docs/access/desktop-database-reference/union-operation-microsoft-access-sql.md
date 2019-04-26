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
# <a name="union-operation-microsoft-access-sql"></a>UNION 操作 (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

ユニオン クエリを作成します。ユニオン クエリとは、独立した複数のクエリまたはテーブルの結果を結合するクエリのことです。

## <a name="syntax"></a>構文

\[TABLE\] *query1* UNION \[ALL\] \[TABLE\] *query2* \[UNION \[ALL\] \[TABLE\] *queryn* \[ … \]\]

UNION 操作には、次の指定項目があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パーツ</p></th>
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


## <a name="remarks"></a>注釈

2 つ以上のクエリ、テーブル、SELECT ステートメントの結果を結合し、1 つの UNION 操作を作成できます。次の例は、「New Accounts」という名前の既存テーブルと SELECT ステートメントを結合したものです。

```sql
TABLE [New Accounts] UNION ALL 
SELECT * 
FROM Customers 
WHERE OrderAmount > 1000;
```

UNION 操作を使用する場合、特に指定しなければ重複したレコードは返されません。ただし、[ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) 述語を使用すると重複分を含むすべてのレコードが必ず返され、クエリの実行速度も速くなります。

UNION 操作でクエリが要求するフィールドの数は、すべてのクエリで同じである必要があります。ただし、フィールドのサイズやデータ型は同じである必要はありません。

エイリアスは最初の SELECT ステートメントでのみ使用します。他のステートメントでは無視されます。ORDER BY 句では、最初の SELECT ステートメントで呼ばれている名前でフィールドが参照されます。

> [!NOTE]
> - 引数 *query* のそれぞれのクエリ中で [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) 句や [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) 句を使用すると、返されるデータをグループ化できます。
> - 引数 *query* の末尾に指定するクエリで [ORDER BY](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/order-by-clause-microsoft-access-sql) 句を使用すると、返されるデータを指定の順序で表示できます。

## <a name="example"></a>例

次の使用例では、ブラジル国内のすべての仕入先および得意先の名前と都市名を取得します。 EnumFields プロシージャを呼び出しますが、このプロシージャについては、SELECT ステートメントの使用例を参照してください。

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
