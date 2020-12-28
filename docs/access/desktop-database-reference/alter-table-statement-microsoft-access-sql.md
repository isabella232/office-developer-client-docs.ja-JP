---
title: ALTER TABLE ステートメント (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 07a83c16368caa6e5c05c7554300c5589a437067
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734183"
---
# <a name="alter-table-statement-microsoft-access-sql"></a>ALTER TABLE ステートメント (Microsoft Access SQL)

**適用先:** Access 2013、Office 2013

[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントで作成されたテーブルのデザインを変更します。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース以外のデータベースの ALTER TABLE または DDL (データ定義言語) ステートメントをサポートしません。 代わりに、DAO の **Create** メソッドをご使用ください。

## <a name="syntax"></a>構文

ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }

ALTER TABLE ステートメントでは、次の引数を使用します。

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
<td><p>変更されるテーブルの名前です。</p></td>
</tr>
<tr class="even">
<td><p><em>field</em></p></td>
<td><p><em>table</em> に対して追加または削除されるフィールドの名前です。 または、<em>table</em> で変更されるフィールドの名前です。</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>
            <em>field</em> のデータ型です。</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>文字数単位のフィールド サイズです (テキスト型とバイナリ型のフィールドのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><em>index</em></p></td>
<td><p><em>field</em> のインデックスです。 このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p><em>table</em> に追加される複数フィールド インデックス定義です。 このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p><em>indexname</em></p></td>
<td><p>削除される複数フィールド インデックスの名前です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

ALTER TABLE ステートメントを使用すると、いくつかの方法で既存のテーブルを変更できます。 以下のことが実行できます。

- ADD COLUMN を使用して新しいフィールドをテーブルに追加します。フィールド名、データ型、および (テキスト型とバイナリ型のフィールドの場合) 省略可能なサイズを指定します。たとえば、次のステートメントでは、Notes という 25 文字のテキスト型フィールドを Employees テーブルに追加します。
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  そのフィールドにインデックスを定義することもできます。 単一フィールド インデックスの詳細については、「[CONSTRAINT 句](constraint-clause-microsoft-access-sql.md)」を参照してください。
    
  フィールドに対して NOT NULL を指定した場合、フィールドには新しいレコードが有効なデータとして必要になります。

- 既存のフィールドのデータ型を変更するには、ALTER COLUMN を使用します。フィールド名、新しいデータ型、および (テキスト型とバイナリ型のフィールドの場合) 省略可能なサイズを指定します。たとえば、次のステートメントでは、Employees テーブルの ZipCode というフィールドの (元は整数として定義されていた) データ型を 10 文字のテキスト型フィールドに変更しています。
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- 複数フィールド インデックスを追加するには、ADD CONSTRAINT を使用します。 複数フィールド インデックスの詳細については、「[CONSTRAINT 句](constraint-clause-microsoft-access-sql.md)」を参照してください。

- フィールドを削除するには、DROP COLUMN を使用します。フィールドの名前のみを指定します。

- 複数フィールド インデックスを削除するには、DROP CONSTRAINT を使用します。予約語の CONSTRAINT に続けて、インデックス名のみを指定します。


> [!NOTE] 
> - 同時に複数のフィールドまたはインデックスを追加または削除することはできません。
> - [CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントを使用すると、単一フィールド インデックスまたは複数フィールド インデックスをテーブルに追加できます。また、ALTER TABLE ステートメントや CREATE INDEX ステートメントで作成したインデックスは、ALTER TABLE ステートメントまたは [DROP](drop-statement-microsoft-access-sql.md) ステートメントを使用して削除できます。
> - NOT NULL を 1 つのフィールドまたは名前付きの CONSTRAINT 句内で使用し、CONSTRAINT という名前の 1 つのフィールドまたは複数のフィールドに適用することができます。 ただし、フィールドに NOT NULL 制限を 1 回だけ適用することができます。 この制限を複数回実行しようすると、実行時エラーになります。

## <a name="example"></a>例

次の使用例では、データ型が通貨型 ( **Money** ) である Salary フィールドを Employees テーブルに追加します。

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

次の使用例では、Salary フィールドのデータ型を通貨型 ( **Money** ) から文字型 ( **Char** ) に変更します。

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Modify the existing Salary field of the Employees table  
        ' by changing it to a CHAR data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

次の使用例では、Salary フィールドを Employees テーブルから削除します。

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

次の使用例では、外部キーを Orders テーブルに追加します。外部キーは、EmployeeID フィールドに基づき、Employees テーブルの EmployeeID フィールドを参照します。この例では、REFERENCES 句の Employees テーブルの後に EmployeeID フィールドをリストする必要はありません。EmployeeID が Employees テーブルの主キーだからです。

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

次の使用例では、外部キーを Orders テーブルから削除します。

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
