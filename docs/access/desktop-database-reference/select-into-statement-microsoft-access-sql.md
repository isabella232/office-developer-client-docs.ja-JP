---
title: SELECT.INTO ステートメント (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 3c5b911c4391dd975c8ed2b1c5ddbf17ccc4bb38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626107"
---
# <a name="selectinto-statement-microsoft-access-sql"></a>SELECT.INTO ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

テーブル作成クエリを作成します。

## <a name="syntax"></a>構文

SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*

SELECT...INTO ステートメントには、次の指定項目があります。

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
<td><p><em>field1</em>、<em>field2</em></p></td>
<td><p>新しいテーブルにコピーするフィールドの名前です。</p></td>
</tr>
<tr class="even">
<td><p><em>newtable</em></p></td>
<td><p>作成するテーブルの名前。名前付け規則に従った名前を指定します。引数 <em>newtable</em> と同じ名前のテーブルが既にある場合は、トラップ可能なエラーになります。</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>外部データベースのパス。パスの記述方法については、「<a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN 句</a>」を参照してください。  </p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>レコードの選択元になる既存テーブルの名前です。このテーブルまたはクエリは 1 つでも複数でも構いません。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

テーブル作成クエリを使用し、レコードをアーカイブしたり、テーブルのバックアップ コピーを作成したり、別のデータベースにエクスポートするか、データを一定期間表示するレポートの基礎として利用するためのコピーを作成したりできます。たとえば、同じテーブル作成クエリを毎月実行し、地域別の月間売上レポートを作成できます。

> [!NOTE]
> - 新規テーブルに主キーを設定する場合があります。テーブル作成クエリで作成したテーブルのフィールドは、クエリの元になるテーブルのフィールドのデータ型とフィールド サイズを継承しますが、それ以外のフィールド プロパティやテーブル プロパティは継承しません。
> - 既存のテーブルにデータを追加するには、SELECT...INTO ステートメントではなく [INSERT INTO](insert-into-statement-microsoft-access-sql.md) ステートメントを使用して追加クエリを作成してください。
> - どのレコードが選択されるかをあらかじめ確認する場合は、テーブル作成クエリを実行する前に、同じ選択条件を使用する [SELECT](select-statement-microsoft-access-sql.md) ステートメントを実行してその結果を調べてください。



## <a name="example"></a>例

この例では、Employees テーブル内のすべてのレコードを選択し、それらを Emp Backup という名前の新しいテーブルにコピーします。

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```
