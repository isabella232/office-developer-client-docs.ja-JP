---
title: ALTER TABLE ステートメント (Microsoft Access SQL)
TOCTitle: ALTER TABLE Statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b8fc826d438973b4d079e9b90d3663ab755821cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479190"
---
# <a name="alter-table-statement-microsoft-access-sql"></a>ALTER TABLE ステートメント (Microsoft Access SQL)


**適用されます**Access 2013 |。Office 2013



[CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントで作成されたテーブルのデザインを変更します。


> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース以外のデータベースの ALTER TABLE または DDL (データ定義言語) ステートメントをサポートしません。代わりに、DAO の Create メソッドを使用してください。



## <a name="syntax"></a>構文

*テーブル*の ALTER TABLE {追加 {*フィールド型*の列の\[(*サイズ*)\] \[NOT NULL\] \[制約*インデックス*\] |ALTER COLUMN*フィールド型*\[(*サイズ*)\] |制約*multifieldindex*} |ドロップ {列の*フィールド*に制約*indexname*}}

ALTER TABLE ステートメントには、次の指定項目があります。

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
<td><p>変更するテーブルの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>field</em></p></td>
<td><p>引数 table に追加、または引数 table から削除するフィールドの名前。または、table で変更するフィールドの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>引数 <em>field</em> のデータ型。</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>バイト数で表したフィールド サイズ。テキスト型 (Text) およびバイナリ型 (Binary) フィールドのみ指定します。</p></td>
</tr>
<tr class="odd">
<td><p><em>index</em></p></td>
<td><p>引数 <em>field</em> のインデックス。このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p>引数 <em>table</em> に追加する複数フィールド インデックスの定義。このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p><em>indexname</em></p></td>
<td><p>削除する複数フィールド インデックスの名前。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

ALTER TABLE ステートメントを使用すると、次の方法で既存のテーブルを変更できます。

  - テーブルに新しいフィールドを追加するには、ADD COLUMN 句を使用します。フィールド名およびデータ型を指定し、テキスト型フィールドとバイナリ型フィールドの場合はサイズ (省略可) も指定します。たとえば、次のステートメントにより、"Notes" という名前の 25 バイトのテキスト型フィールドが Employees テーブルに追加されます。
    
    ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
    ```
    
    また、追加したフィールドにインデックスを定義することもできます。単一フィールド インデックスの詳細については、「[CONSTRAINT 句](constraint-clause-microsoft-access-sql.md)」を参照してください。
    
    フィールドに対して NOT NULL を指定した場合、フィールドには新しいレコードが有効なデータとして必要になります。

  - 既存のフィールドのデータ型を変更するには、ALTER COLUMN 句を使用します。フィールド名および新しいデータ型を指定し、テキスト型フィールドとバイナリ型フィールドの場合はサイズ (省略可) も指定します。たとえば、次のステートメントでは、Employees テーブルにある "ZipCode" という名前のフィールドのデータ型を整数型から 10 バイトのテキスト型に変更します。
    
    ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
    ```

  - 複数フィールド インデックスを追加するには、ADD CONSTRAINT 句を使用します。複数フィールド インデックスの詳細については、「[CONSTRAINT 句](constraint-clause-microsoft-access-sql.md)」を参照してください。

  - フィールドを削除するには、DROP COLUMN 句を使用します。フィールド名のみを指定します。

  - 複数フィールド インデックスを削除するには、DROP CONSTRAINT 句を使用します。予約語 CONSTRAINT の後にインデックス名のみを指定します。


> [!NOTE]
> <UL>
> <LI>
> <P>一度に複数のフィールドおよびインデックスを追加または削除することはできません。</P>
> <LI>
> <P><A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A> ステートメントを使用すると、単一フィールド インデックスまたは複数フィールド インデックスをテーブルに追加できます。また、ALTER TABLE ステートメントや CREATE INDEX ステートメントで作成したインデックスは、ALTER TABLE ステートメントまたは <A href="drop-statement-microsoft-access-sql.md">DROP</A> ステートメントを使用して削除できます。</P>
> <LI>
> <P>NOT NULL は、単一フィールド、または名前付き CONSTRAINT 句の内部で使用できます。名前付き CONSTRAINT 句は、単一フィールドまたは複数フィールドのどちらかの名前付き CONSTRAINT 句に適用されます。ただし、NOT NULL の制約を適用できるのはフィールドに対して一度のみです。再度適用しようとした場合は実行時エラーになります。 
</P></LI></UL>



## <a name="example"></a>使用例

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
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
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
