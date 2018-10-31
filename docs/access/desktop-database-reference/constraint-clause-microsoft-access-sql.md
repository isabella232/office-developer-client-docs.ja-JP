---
title: 制約句 (Microsoft Access SQL)
TOCTitle: CONSTRAINT clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 87870d824f9e26f601529bc60b737f1e46b12960
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863004"
---
# <a name="constraint-clause-microsoft-access-sql"></a>制約句 (Microsoft Access SQL)

**適用されます**Access 2013 |。Office 2013

CONSTRAINT (制約) はインデックスに似ています。インデックスと違う点は、他のテーブルとのリレーションシップも設定できることです。

CONSTRAINT 句は、[ALTER TABLE](alter-table-statement-microsoft-access-sql.md) ステートメントおよび [CREATE TABLE](create-table-statement-microsoft-access-sql.md) ステートメントの中で制約を作成または削除する場合に使用します。CONSTRAINT 句には、単一フィールドの制約を作成するものと、複数フィールドの制約を作成するものの 2 種類があります。

> [!NOTE]
> [!メモ] Microsoft Access データベース エンジンは、Microsoft Access データベース エンジン以外のデータベースでは CONSTRAINT 句や DDL (データ定義言語) ステートメントを使用できません。 代わりに DAO の**Create**メソッドを使用します。

## <a name="syntax"></a>構文

**単一フィールド制約**の場合:

制約*名*{主キー。固有 |NOT NULL。参照*外部テーブル* \[(*foreignfield1、foreignfield2*)\] \[ON UPDATE CASCADE |設定 NULL\] \[ON DELETE CASCADE |NULL 設定\]}

**複数フィールド制約**の場合:

制約*名*{0} プライマリ ・ キー (*primary1*\[、 *primary2* \[、.\]\]) |一意 (*unique 1*\[、 *unique2* \[、.\]\]) |NOT NULL (*notnull1*\[、 *notnull2* \[、.\]\]) |外部キー\[インデックスのない\](*範囲 1*\[、 *ref2* \[、.\] \]) の参照*外部テーブル* \[(*foreignfield1* \[、 *foreignfield2* \[、.\] \])\] \[ON UPDATE CASCADE |設定 NULL\] \[ON DELETE CASCADE |NULL 設定\]}

CONSTRAINT 句には、次の指定項目があります。

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
<td><p><em>name</em></p></td>
<td><p>作成する制約の名前。</p></td>
</tr>
<tr class="even">
<td><p><em>primary1</em>, <em>primary2</em></p></td>
<td><p>主キーに指定するフィールドの名前。複数指定もできます。</p></td>
</tr>
<tr class="odd">
<td><p><em>unique1</em>, <em>unique2</em></p></td>
<td><p>一意なキーに指定するフィールドの名前。複数指定もできます。</p></td>
</tr>
<tr class="even">
<td><p><em>notnull1, notnull2</em></p></td>
<td><p>非 Null 値に制限されるフィールドの名前。複数指定もできます。</p></td>
</tr>
<tr class="odd">
<td><p><em>ref1</em>, <em>ref2</em></p></td>
<td><p>別のテーブルにあるフィールドを参照する外部キー フィールドの名前。複数指定もできます。</p></td>
</tr>
<tr class="even">
<td><p><em>foreigntable</em></p></td>
<td><p>引数 <em>foreignfield</em> で指定した 1 つ以上のフィールドのある外部キー側のテーブルの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>foreignfield1</em>, <em>foreignfield2</em></p></td>
<td><p>引数 <em>ref1</em>、<em>ref2</em> で指定した引数 <em>foreigntable</em> の 1 つ以上のフィールドの名前。参照されるフィールドが引数 <em>foreigntable</em> の主キーである場合は、この句を省略できます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

単一フィールドの CONSTRAINT 構文は、ALTER TABLE ステートメントや CREATE TABLE ステートメントなどのフィールド定義句の中で、フィールド データ型の指定の直後に記述します。

ALTER TABLE ステートメントや CREATE TABLE ステートメントのフィールド定義句以外の箇所で予約語 CONSTRAINT を使用する場合は、必ず複数フィールドの CONSTRAINT 構文を使用します。

CONSTRAINT 句を使用すると、次のいずれかの制約をフィールドに適用できます。

- 予約語 UNIQUE を使用すると、フィールドを一意なキーとして指定できます。この結果、テーブルでこのフィールドの値を 2 つのレコードに同時に設定することはできなくなります。どのフィールドでも一意なキーに指定することができます。数にも制限はありません。複数フィールドの制約を一意なキーとして指定した場合は、インデックス内のすべてのフィールドの値の組み合わせが重複しないようにする必要があります。1 つのフィールドのみで複数のレコードが同じ値を持っている場合も同様です。

- 予約語 PRIMARY KEY を使用すると、テーブル内の 1 つ以上のフィールド セットを主キーとして指定できます。主キーの値はすべて **Null** 値以外の一意な値である必要があります。1 つのテーブルに指定できる主キーは 1 つのみです。
    
  > [!NOTE]
  > [!メモ] 既に主キーが設定されているテーブルには PRIMARY KEY 制約を設定しないでください。設定した場合はエラーになります。

- 予約語 FOREIGN KEY を使用すると、指定したフィールドを外部キーにすることができます。外部キー側のテーブルの主キーが複数のフィールドから成る場合は、必ず複数フィールドの制約の定義を使用し、すべての参照元フィールド、外部キー側のテーブル名、および外部キー側のテーブルのすべての参照先フィールドの名前を、それぞれ指定してください。この場合は、参照先フィールドは参照元フィールドと同じ順序で指定してください。既定では、データベース エンジンは外部キー側のテーブルの主キーを参照先フィールドと見なします。このため、参照先フィールドが外部キー側のテーブルの主キーである場合は、参照先フィールドを指定する必要ありません。 外部キーの制約は、対応する主キーの値が変更されるときに行われる特定の動作を定義します。

- 外部キー側のテーブルで行われる動作を指定することができます。この指定は、CONSTRAINT が定義されるテーブルの対応する主キーで行われる動作に基づきます。たとえば、Customers テーブルに関して次のような定義を考えます。
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Orders テーブルの次のような定義を考えます。この Orders テーブルは、Customers テーブルの主キーを参照する外部キーのリレーションシップを定義しています。
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  ON UPDATE CASCADE 句と ON DELETE CASCADE 句は、どちらも外部キー上に定義されます。ON UPDATE CASCADE 句は、Customers テーブルで顧客の情報 (CustId) が更新された場合、この更新が Orders テーブルをとおしてカスケードされることを意味します。各注文に含まれる、対応した顧客情報の値は、自動的に新しい値に更新されます。ON DELETE CASCADE 句は、Customers テーブルで顧客が削除された場合、Orders テーブルにある同じ顧客の顧客情報の値を含む行もすべて同様に削除されることを意味します。 CASCADE アクションの代わりに SET NULL アクションを使う、次のような Orders テーブルの異なる定義について検討します。
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  ON UPDATE SET NULL 句は、Customers テーブルで顧客の情報 (CustId) が更新された場合、Orders テーブルの対応する外部キーの値が自動的に NULL に設定されることを意味します。同様に、ON UPDATE SET NULL 句は、顧客が Customers テーブルから削除された場合、Orders テーブルの対応するすべての外部キーの値が、自動的に NULL に設定されることを意味します。

外部キーに自動的にインデックスが作成されることを防ぐために、修飾子 NO INDEX を使用できます。この外部キーを定義する形式は、結果としてインデックスの値が頻繁に繰り返される場合に限り使用してください。外部キーのインデックスの値が頻繁に繰り返される中でインデックスを使用することは、単にテーブルのスキャンを行うよりも能率が下がります。テーブルから挿入や削除された行と一緒にこの種のインデックスを保守することは、パフォーマンスを下げるばかりで何の利益も生み出しません。

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

<br/>

