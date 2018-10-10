---
title: CREATE TABLE ステートメント (Microsoft Access SQL)
TOCTitle: CREATE TABLE Statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 749d593a0c9ed32290ee91aec20c79a141a83f56
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477855"
---
# <a name="create-table-statement-microsoft-access-sql"></a>CREATE TABLE ステートメント (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013

新しいテーブルを作成します。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CREATE TABLE 句や DDL (データ定義言語) ステートメントを使用できません。Microsoft Access データベース エンジン以外のデータベースでは代わりに DAO の Create 系メソッドを使用してください。

## <a name="syntax"></a>構文

作成\[一時\]テーブルの*テーブル*(*フィールド 1 種類* \[(*サイズ*)\] \[NOT NULL\] \[で圧縮。COMP と\] \[ *index1* \] \[、 *field2* *型* \[(*サイズ*)\] \[NOT NULL\] \[ *index2* \] \[、.\] \] \[、制約*multifieldindex* \[、.\]\])

CREATE TABLE ステートメントには、次の指定項目があります。

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
<td><p>作成するテーブルの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>新しいテーブルに作成するフィールドの名前。少なくとも 1 つのフィールドを作成する必要があります。</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>新規テーブルの<em>フィールド</em>のデータ型です。</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>バイト数で表したフィールド サイズ。テキスト型 (Text) およびバイナリ型 (Binary) フィールドのみ指定します。</p></td>
</tr>
<tr class="odd">
<td><p><em>index1</em>, <em>index2</em></p></td>
<td><p>単一フィールドを定義する CONSTRAINT 句。このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。  </p></td>
</tr>
<tr class="even">
<td><p><em>multifieldindex</em></p></td>
<td><p>複数フィールドを定義する CONSTRAINT 句。このインデックスの作成方法については、「<a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT 句</a>」を参照してください。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

CREATE TABLE ステートメントを使用すると、新しいテーブルとそのフィールド、およびフィールドの制約を定義できます。フィールドに対して NOT NULL を指定した場合、フィールドには新しいレコードが有効なデータとして必要になります。

CONSTRAINT 句はフィールドに対してさまざまな制約を設定するもので、これを使用して主キーを設定することができます。また、[CREATE INDEX](create-index-statement-microsoft-access-sql.md) ステートメントを使用して、既存のテーブルに主キーまたは追加のインデックスを作成することもできます。

NOT NULL は、単一フィールド、または名前付き CONSTRAINT 句の内部で使用できます。名前付き CONSTRAINT 句は、単一フィールドまたは複数フィールドのどちらかの名前付き CONSTRAINT 句に適用されます。ただし、NOT NULL の制約を適用できるのはフィールドに対して一度のみです。再度適用しようとした場合は実行時エラーになります。

一時テーブルが作成される場合、作成されたセッションの中でのみ見ることができます。セッションが終了すると、自動的に削除されます。一時テーブルは、複数のユーザーからアクセスすることができます。

WITH COMPRESSION 属性には、テキスト型 (Text) であるメモ型 (Memo) や文字型 (Character) および類似のデータ型のみ使用できます。

Unicode 文字の表示形式に変更するために、WITH COMPRESSION 属性が CHARACTER 列に追加されました。Unicode 文字には、各文字一律に 2 バイトを必要とします。これは、主に文字データを含む既存の Microsoft® Jet データベースを Microsoft Access データベース エンジンの形式に変換すると、ファイル サイズが約 2 倍になることを意味します。しかし、Unicode 表示形式の文字セットの多くは、以前 1 バイトの文字セット (SBCS) であり、簡単に 1 バイトに圧縮することが可能です。CHARACTER 列をこの属性で定義すると、データが格納時には自動的に圧縮され、取得時には圧縮解除されるようになります。

MEMO 列もデータの格納を圧縮形式で定義することができます。ただし、これには制限があります。圧縮時 4096 バイト以下になる MEMO 列のインスタンスのみ圧縮されます。それ以外の MEMO 列のインスタンスは圧縮されずに残ります。これは、所定のテーブルの所定の MEMO 列で、圧縮されたデータと圧縮されていないデータが混在している可能性があることを意味します。

## <a name="example"></a>使用例

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
