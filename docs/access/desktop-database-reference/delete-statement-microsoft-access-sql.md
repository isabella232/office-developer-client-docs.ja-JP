---
title: ステートメント (Microsoft Access SQL) を削除します。
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
ms.openlocfilehash: 5ce152e790fb2d57ed607f88feb155fe99bd5850
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878494"
---
# <a name="delete-statement-microsoft-access-sql"></a>ステートメント (Microsoft Access SQL) を削除します。

**適用されます**Access 2013、Office 2013。

[FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) 句で指定したテーブルから [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) 句の条件を満たすレコードを削除する削除クエリを作成します。

## <a name="syntax"></a>構文

削除\[*テーブル*です。\* \] *テーブル*から、*抽出条件*

DELETE ステートメントには、次の指定項目があります。

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
<td><p><em>table</em></p></td>
<td><p>削除するレコードのあるテーブルの名前。この項目は省略可能です。</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>削除するレコードのあるテーブルの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>削除するレコードを決める式。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

DELETE ステートメントは、多数のレコードを削除する場合に特に便利です。

データベースからあるテーブル全体を削除するには、**DROP** ステートメントで [Execute](drop-statement-microsoft-access-sql.md) メソッドを使用します。ただし、テーブルを削除するとテーブルの構造も失われます。これに対して、DELETE ステートメントを使用した場合はデータのみが削除され、テーブルの構造や、フィールド属性、インデックスなどのテーブル プロパティはすべてそのまま残されます。

DELETE ステートメントを使用すると、あるテーブルとの間に一対多リレーションシップがある複数のテーブルからレコードを削除できます。連鎖削除を行うと、"一" 側のテーブルに含まれるレコードがクエリで削除された場合に、"多" 側にある対応するレコードも削除されます。たとえば、[得意先] テーブルと [注文] テーブルとの間にリレーションシップが設定されていて、[得意先] テーブルが "一" 側、[注文] テーブルが "多" 側であるとします。この場合、連鎖削除オプションが指定されていれば、[得意先] テーブルからレコードを削除すると、それに対応する [注文] テーブルのレコードも削除されます。

削除クエリでは、レコード全体が削除されます。特定のフィールドのデータのみを削除することはできません。特定のフィールド値を削除する場合は、値を **Null** 値に変更する更新クエリを作成します。

> [!IMPORTANT]
> - 特定のフィールド値を削除する場合は、値を Null 値に変更する更新クエリを作成します。
> - 削除クエリでいったん削除したレコードは、元に戻せません。

## <a name="example"></a>使用例

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
