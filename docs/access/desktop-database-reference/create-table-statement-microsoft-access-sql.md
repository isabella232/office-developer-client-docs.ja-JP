---
title: CREATE TABLE ステートメント (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/03/2019
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 5aea8694c450764f686c226554041da13179aead
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615726"
---
# <a name="create-table-statement-microsoft-access-sql"></a>CREATE TABLE ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

新しいテーブルを作成します。

> [!NOTE]
> Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CREATE TABLE 句や DDL (データ定義言語) ステートメントを使用できません。Microsoft Access データベース エンジン以外のデータベースでは代わりに DAO の **Create** 系メソッドを使用してください。

## <a name="syntax"></a>構文

CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])

CREATE TABLE ステートメントでは、次の引数を使用します。

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
<td><p>作成されるテーブルの名前です。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>、<em>field2</em></p></td>
<td><p>新しいテーブルを作成するフィールドの名前です。1 つ以上のフィールドを作成する必要があります。</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>新しいテーブルの<em>フィールド</em>のデータ型。</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>文字数単位のフィールド サイズです (テキスト型とバイナリ型のフィールドのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><em>index1</em>、<em>index2</em></p></td>
<td><p>単一フィールド インデックスを定義する CONSTRAINT 句です。 このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p>複数フィールド インデックスを定義する CONSTRAINT 句です。 このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

CREATE TABLE ステートメントを使用して、新しいテーブル、フィールド、およびフィールドの制約を定義します。 フィールドに対して NOT NULL を指定した場合、フィールドには新しいレコードが有効なデータとして必要になります。

CONSTRAINT 句はフィールドに対してさまざまな制約を設定するもので、これを使用して主キーを設定することができます。また、[CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントを使用して、既存のテーブルに主キーまたは追加のインデックスを作成することもできます。

NOT NULL を 1 つのフィールドまたは名前付きの CONSTRAINT 句内で使用し、CONSTRAINT という名前の 1 つのフィールドまたは複数のフィールドに適用することができます。ただし、フィールドに NOT NULL 制限を 1 回だけ適用することができます。この制限を複数回実行しようすると、実行時エラーになります。

一時テーブルが作成される場合、作成されたセッションの中でのみ見ることができます。セッションが終了すると、自動的に削除されます。一時テーブルは、複数のユーザーからアクセスすることができます。

WITH COMPRESSION 属性は、CHARACTER および MEMO (TEXT とも呼ばれます) データ型およびそれらの類義語でのみ使用できます。

Unicode 文字の表示形式に変更するために、WITH COMPRESSION 属性が CHARACTER 列に追加されました。Unicode 文字には、各文字一律に 2 バイトを必要とします。これは、主に文字データを含む既存の Microsoft Jet データベースを Microsoft Access データベース エンジンの形式に変換すると、ファイル サイズが約 2 倍になることを意味します。しかし、Unicode 表示形式の文字セットの多くは、以前 1 バイトの文字セット (SBCS) であり、簡単に 1 バイトに圧縮することが可能です。CHARACTER 列をこの属性で定義すると、データが格納時には自動的に圧縮され、取得時には圧縮解除されるようになります。

MEMO 型の列を定義すると、圧縮形式でデータを格納することもできます。ただし、これには制限があります。MEMO 型の列のインスタンスが、圧縮されるときには、4096 バイト以内のみが圧縮されます。MEMO 型の列の他のすべてのインスタンスは圧縮されません。これは、特定のテーブル内の MEMO 型の列で、データの一部が圧縮され、一部のデータが圧縮されていないことを意味します。

## <a name="example"></a>例

次の使用例では、2 つのテキスト フィールドを含む "ThisTable" という名前の新しいテーブルを作成します。

```vb
    Sub CreateTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with two text fields. 
        dbs.Execute "CREATE TABLE ThisTable " _ 
            & "(FirstName CHAR, LastName CHAR);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

次の使用例では、テキスト フィールド 2 つと日付/時刻型 (Date/Time) フィールド、および 3 つのフィールドすべてから作成された一意のインデックスを含む、"MyTable" というテーブルを作成します。

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

次の使用例では、2 つのテキスト フィールドおよび整数型 ( **Integer** ) フィールドを含む新しいテーブルを作成します。SSN フィールドは主キーです。

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```

<br/>

次の使用例では、すべての異なるフィールドとインデックスの種類を示す`~~Kitsch'n Sync`という新しいテーブルを作成します。 AutoNumber フィールドが主キーです。

```vb
    Sub CreateTableX6()
        On Error Resume Next
        Application.CurrentDb.Execute "Drop Table [~~Kitsch'n Sync];"
        On Error GoTo 0
        
        'This example uses ADODB instead of the DAO shown in the previous
        'ones because DAO does not support the DECIMAL and GUID data types
        Dim con As ADODB.Connection
        Set con = CurrentProject.Connection
        con.Execute "" _
            & "CREATE TABLE [~~Kitsch'n Sync](" _
                & " [Auto]                  COUNTER" _
                & ",[Byte]                  BYTE" _
                & ",[Integer]               SMALLINT" _
                & ",[Long]                  INTEGER" _
                & ",[Single]                REAL" _
                & ",[Double]                FLOAT" _
                & ",[Decimal]               DECIMAL(18,5)" _
                & ",[Currency]              MONEY" _
                & ",[ShortText]             CHAR" _
                & ",[LongText]              MEMO" _
                & ",[PlaceHolder1]          MEMO" _
                & ",[DateTime]              DATETIME" _
                & ",[YesNo]                 BIT" _
                & ",[OleObject]             IMAGE" _
                & ",[ReplicationID]         UNIQUEIDENTIFIER" _
                & ",[Required]              INTEGER NOT NULL" _
                & ",[Unicode Compression]   MEMO WITH COMP" _
                & ",[Indexed]               INTEGER" _
                & ",CONSTRAINT [PrimaryKey] PRIMARY KEY ([Auto])" _
                & ",CONSTRAINT [Unique Index] UNIQUE ([Byte],[Integer],[Long])" _
            & ");"
        con.Execute "CREATE INDEX [Single-Field Index] ON [~~Kitsch'n Sync]([Indexed]);"
        con.Execute "CREATE INDEX [Multi-Field Index] ON [~~Kitsch'n Sync]([Auto],[Required]);"
        con.Execute "CREATE INDEX [IgnoreNulls Index] ON [~~Kitsch'n Sync]([Single],[Double]) WITH IGNORE NULL;"
        con.Execute "CREATE UNIQUE INDEX [Combined Index] ON [~~Kitsch'n Sync]([ShortText],[LongText]) WITH IGNORE NULL;"
        Set con = Nothing
    
        'Add a Hyperlink Field
        Dim AllDefs As DAO.TableDefs, TblDef As DAO.TableDef, Fld As DAO.Field
        Set AllDefs = Application.CurrentDb.TableDefs
        Set TblDef = AllDefs("~~Kitsch'n Sync")
        Set Fld = TblDef.CreateField("Hyperlink", dbMemo)
        Fld.Attributes = dbHyperlinkField + dbVariableField
        Fld.OrdinalPosition = 10
        TblDef.Fields.Append Fld
        
        DoCmd.RunSQL "ALTER TABLE [~~Kitsch'n Sync] DROP COLUMN [PlaceHolder1];"
    End Sub
```
