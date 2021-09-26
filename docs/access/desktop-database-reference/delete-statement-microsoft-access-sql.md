---
title: DELETE ステートメント (Microsoft Access SQL)
TOCTitle: DELETE statement (Microsoft Access SQL)
ms:assetid: 64c235bc-5b1a-0a33-714a-9933ba7a81e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195097(v=office.15)
ms:contentKeyID: 48545299
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277573
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 5eba43d04f1d0eccf1b7e0ce63c6c6aedd3946d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618246"
---
# <a name="delete-statement-microsoft-access-sql"></a>DELETE ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

[FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句で指定したテーブルから [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句の条件を満たすレコードを削除する削除クエリを作成します。

## <a name="syntax"></a>構文

DELETE \[*table*.\*\] FROM *table* WHERE *criteria*

DELETE ステートメントでは次の引数を使用します。

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
<td><p><em>table</em></p></td>
<td><p>レコードを削除するテーブルのオプションの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>レコードを削除するテーブルの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>削除するレコードを決める式。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

DELETE は、多くのレコードを削除する場合に特に便利です。

データベースからあるテーブル全体を削除するには、**DROP** ステートメントで [Execute](drop-statement-microsoft-access-sql.md) メソッドを使用します。ただし、テーブルを削除するとテーブルの構造も失われます。これに対して、DELETE ステートメントを使用した場合はデータのみが削除され、テーブルの構造や、フィールド属性、インデックスなどのテーブル プロパティはすべてそのまま残されます。

DELETE ステートメントを使用すると、あるテーブルとの間に一対多リレーションシップがある複数のテーブルからレコードを削除できます。連鎖削除を行うと、"一" 側のテーブルに含まれるレコードがクエリで削除された場合に、"多" 側にある対応するレコードも削除されます。たとえば、[得意先] テーブルと [注文] テーブルとの間にリレーションシップが設定されていて、[得意先] テーブルが "一" 側、[注文] テーブルが "多" 側であるとします。この場合、連鎖削除オプションが指定されていれば、[得意先] テーブルからレコードを削除すると、それに対応する [注文] テーブルのレコードも削除されます。

削除クエリでは、レコード全体が削除されます。特定のフィールドのデータのみを削除することはできません。特定のフィールド値を削除する場合は、値を **Null** 値に変更する更新クエリを作成します。

> [!IMPORTANT]
> - 特定のフィールド値を削除する場合は、値を Null 値に変更する更新クエリを作成します。
> - データのバックアップ コピーは常に保持しておきます。間違ったレコードを削除した場合、バックアップ コピーからレコードを元に戻すことができます。

## <a name="example"></a>例

次の使用例では、役職が Trainee である社員のすべてのレコードを削除します。FROM 句に 1 つのテーブルのみが含まれている場合は、テーブル名を DELETE ステートメントにリストする必要はありません。

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
