---
title: DROP ステートメント (Microsoft Access SQL)
TOCTitle: DROP statement (Microsoft Access SQL)
ms:assetid: a8c79c35-22da-2e6d-88b5-620eb481bb61
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821409(v=office.15)
ms:contentKeyID: 48546907
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f31067c96c19804352ca74957e064f9338b49260
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293652"
---
# <a name="drop-statement-microsoft-access-sql"></a>DROP ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

データベースから既存のテーブル、プロシージャ、またはビューを削除するか、テーブルから既存のインデックスを削除します。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは DROP 句や DDL (データ定義言語) ステートメントを使用できません。Microsoft Access データベース エンジン以外のデータベースでは、代わりに DAO の **Delete** 系メソッドを使用してください。

## <a name="syntax"></a>構文

DROP {TABLE *table* | INDEX *index* ON *table* | PROCEDURE *procedure* | VIEW *view*}

DROP ステートメントには、次の指定項目があります。

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
<td><p>削除されるテーブル、またはインデックスが削除されるテーブルの名前です。</p></td>
</tr>
<tr class="even">
<td><p><em>procedure</em></p></td>
<td><p>削除されるプロシージャの名前です。</p></td>
</tr>
<tr class="odd">
<td><p><em>view</em></p></td>
<td><p>削除されるビューの名前です。</p></td>
</tr>
<tr class="even">
<td><p><em>index</em></p></td>
<td><p>
            <em>テーブル</em>から削除されるインデックスの名前です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

テーブルを削除したり、テーブルからインデックスを削除したりするには、テーブルを閉じる必要があります。

[ALTER TABLE](alter-table-statement-microsoft-access-sql.md) ステートメントを使用してもテーブルからインデックスを削除できます。

[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントを使用すると、テーブルを作成できます。 [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントまたは ALTER TABLE ステートメントを使用すると、インデックスを作成できます。テーブルを変更するには、ALTER TABLE ステートメントを使用します。

## <a name="example"></a>例

次の使用例では、Northwind データベースの Employees テーブルに架空の NewIndex インデックスが存在していることを前提としています。

次の使用例では、MyIndex インデックスを Employees テーブルから削除します。

```vb
    Sub DropX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete NewIndex from the Employees table. 
        dbs.Execute "DROP INDEX NewIndex ON Employees;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

次の使用例では、Employees テーブルをデータベースから削除します。

```vb
    Sub DropX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Employees table. 
        dbs.Execute "DROP TABLE Employees;" 
     
        dbs.Close 
     
    End Sub
```
