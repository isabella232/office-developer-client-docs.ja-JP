---
title: CREATE TABLE ステートメント (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 296e1405245d6204d136888e78b6a3846b468a1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295360"
---
# <a name="create-table-statement-microsoft-access-sql"></a>CREATE TABLE ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

新しいテーブルを作成します。

> [!NOTE]
> Microsoft Access データベース エンジンでは、Microsoft Access データベース エンジン以外のデータベースで CREATE TABLE やその他の DDL ステートメントを使用することはできません。 代わりに、DAO の **Create** メソッドを使用してください。

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

TEMPORARY テーブルが作成される場合、作成されたセッションの中でのみ見ることができます。 セッションの終了時に自動的に削除されます。 一時テーブルは、複数のユーザーによってアクセスできます。

WITH COMPRESSION 属性は、CHARACTER および MEMO (TEXT とも呼ばれます) データ型およびそれらの類義語でのみ使用できます。

Unicode 文字表現形式の変更のために、WITH COMPRESSION 属性が、CHARACTER 列に追加されました。 Unicode 文字では、各文字を格納するのにそれぞれ 2 バイトが必要です。 これは、主に文字データを含む既存の Microsoft Jet データベースを Microsoft Access データベース エンジンの形式に変換すると、ファイル サイズが約 2 倍になることを意味します。 しかし、Unicode 表示形式の文字セットの多くは、以前 1 バイトの文字セット (SBCS) であり、簡単に 1 バイトに圧縮することが可能です。 この属性を使用して CHARACTER 型の列を定義すると、列への格納時のデータ圧縮と列からの取得時のデータ圧縮解除が自動的に実行されます。

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
