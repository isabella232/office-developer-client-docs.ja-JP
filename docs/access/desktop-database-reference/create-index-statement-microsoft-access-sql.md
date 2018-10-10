---
title: CREATE INDEX ステートメント (Microsoft Access SQL)
TOCTitle: CREATE INDEX Statement (Microsoft Access SQL)
ms:assetid: c5919ef4-a08d-df06-7078-5331adbcb45c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823109(v=office.15)
ms:contentKeyID: 48547612
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277562
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ab501348d19ad8577bf1a55a3f37c6c3923381b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476596"
---
# <a name="create-index-statement-microsoft-access-sql"></a>CREATE INDEX ステートメント (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013

既存のテーブルに新しいインデックスを作成します。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CREATE INDEX ステートメントや DDL (データ定義言語) ステートメントを使用できません。ただし、CREATE INDEX ステートメントを使用して ODBC リンク テーブルに擬似インデックスを作成することは可能です。Microsoft Access データベース エンジン以外のデータベースでは代わりに DAO の Create 系メソッドを使用してください。詳細については、後の「解説」を参照してください。

## <a name="syntax"></a>構文

作成\[独自の\]*インデックス*の*テーブル*のインデックス (*フィールド* \[ASC |DESC\]\[、*フィールド* \[ASC |DESC\]をしています.\]) \[WITH {主 |NULL を許可しません。NULL を無視します。\]

CREATE INDEX ステートメントには次の指定項目があります。

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
<td><p><em>index</em></p></td>
<td><p>作成するインデックスの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>table</em></p></td>
<td><p>インデックスを作成する既存のテーブルの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>field</em></p></td>
<td><p>インデックスを付けるフィールドの名前。単一フィールド インデックスを作成するには、テーブル名の後にフィールド名をかっこで囲んで指定します。複数フィールド インデックスを作成するには、インデックスを設定するフィールドの名前をすべて列挙します。また、降順のインデックスを作成するには、予約語 DESC を使用します。DESC による指定がなければ昇順と見なされます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

インデックス フィールドの値がレコード間で重複しないようにするには、予約語 UNIQUE を使用します。

WITH 句を併用すると、次の方法でデータの入力規則を設定できます。

- DISALLOW NULL オプションを使用すると、新しいレコードのインデックス フィールドに Null 値を入力できなくなります。

- IGNORE NULL オプションを使用すると、インデックス フィールドに **Null** 値が格納されているレコードを、インデックスに入れることができなくなります。

- 予約語 PRIMARY を使用すると、インデックス フィールドを主キーとして指定します。これによりキーが一意な値になるため、予約語 UNIQUE は省略できます。

CREATE INDEX ステートメントを使用すると、Microsoft® SQL Server のような、インデックスを持たない ODBC データ ソースのリンク テーブルに、擬似インデックスを作成することができます。この場合は、リモート サーバーへの権限やアクセス権は必要ありません。また、擬似インデックスの作成はリモート データベースには通知されず、リモート データベースに影響を与えることもありません。リンク テーブルの場合でも、通常のテーブルの場合と同じ構文を使用します。したがって、通常は読み取り専用になっているテーブルに擬似インデックスを作成すると便利です。

[ALTER TABLE](alter-table-statement-microsoft-access-sql.md) ステートメントを使用して、テーブルに単一フィールド インデックスまたは複数フィールド インデックスを追加することもできます。ALTER TABLE ステートメントや CREATE INDEX ステートメントで作成したインデックスは、ALTER TABLE ステートメントまたは [DROP](drop-statement-microsoft-access-sql.md) ステートメントを使用して削除できます。

> [!NOTE]
> [!メモ] 既に主キーが設定されているテーブルに新しいインデックスを作成する場合は、予約語 PRIMARY は使用しないでください。使用した場合はエラーになります。

## <a name="example"></a>使用例

次の使用例では、Employees テーブルの "Home Phone" および "Extension" というフィールドで構成されたインデックスを作成します。

```vb
    Sub CreateIndexX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create the NewIndex index on the Employees table. 
        dbs.Execute "CREATE INDEX NewIndex ON Employees " _ 
            & "(HomePhone, Extension);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

次の使用例では、CustomerID フィールドを使用して Customers テーブルにインデックスを作成します。CustomerID フィールドの 2 つのレコードに同じデータを入れることはできません。また、Null 値も入力できません。

```vb
    Sub CreateIndexX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a unique index, CustID, on the  
        ' CustomerID field. 
        dbs.Execute "CREATE UNIQUE INDEX CustID " _ 
            & "ON Customers (CustomerID) " _ 
            & "WITH DISALLOW NULL;" 
     
        dbs.Close 
     
    End Sub
```
