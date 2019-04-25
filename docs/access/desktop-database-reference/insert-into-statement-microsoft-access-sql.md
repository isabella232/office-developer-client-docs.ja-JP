---
title: INSERT INTO ステートメント (Microsoft Access SQL)
TOCTitle: INSERT INTO statement (Microsoft Access SQL)
ms:assetid: d3e44258-79f2-caba-8629-bde03f898f2d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834799(v=office.15)
ms:contentKeyID: 48547918
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277575
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 4fee5e9e8878274f2c20dd83a3dbedaf2903ca62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291334"
---
# <a name="insert-into-statement-microsoft-access-sql"></a>INSERT INTO ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

1 つのテーブルに 1 つのレコードまたは複数のレコードを追加します。 追加クエリとも呼ばれます。

## <a name="syntax"></a>構文

### <a name="multiple-record-append-query"></a>複数レコード追加クエリ

INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] \[IN *externaldatabase*\] SELECT \[*source*.\]*field1*\[, *field2*\[, …\] FROM *tableexpression*

### <a name="single-record-append-query"></a>単一レコード追加クエリ:

INSERT INTO *target* \[(*field1*\[, *field2*\[, …\]\])\] VALUES (*value1*\[, *value2*\[, …\])

INSERT INTO ステートメントには、次の指定項目があります。

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
<td><p><em>target</em></p></td>
<td><p>レコードを追加するテーブルまたはクエリの名前です。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>, <em>field2</em></p></td>
<td><p>
            <em>target</em> 引数に続く場合、データを追加するフィールド名です。<em>source</em> 引数に続く場合、データを取得するフィールド名です。</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>外部データベースのパス。パスの記述方法については、「<a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN 句</a>」を参照してください。  </p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>レコードをコピーするテーブルまたはクエリの名前です。</p></td>
</tr>
<tr class="odd">
<td><p><em>tableexpression</em></p></td>
<td><p>挿入するレコードのある 1 つ以上のテーブルの名前。単一のテーブル名、保存されたクエリ名、または <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>、<a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>、<a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> のいずれかの操作の結果としてできる複合テーブルを指定します。  </p></td>
</tr>
<tr class="even">
<td><p><em>value1</em>、<em>value2</em></p></td>
<td><p>新しいレコードの特定のフィールドに挿入する値です。各値は、一覧内の値の位置と対応するフィールドに挿入されます。つまり、<em>value1</em> は新しいレコードの <em>field1</em> に挿入され、<em>value2</em> は <em>field2</em>に、というように挿入されます。値はコンマで区切り、テキスト フィールドは引用符 (' ') で囲む必要があります。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

INSERT INTO ステートメントで 1 つのレコードを追加するには、上記のように単一レコード追加クエリの構文を使用します。この場合は、レコードの各フィールドの名前と値を指定します。また、値を割り当てるフィールドと、そのフィールドに割り当てる値を指定します。指定していないフィールドには、既定値または **Null** 値が挿入されます。レコードはテーブルの末尾に追加されます。

また、INSERT INTO ステートメントを使用して、別のテーブルからレコードのセットを追加することもできます。これには、上記の複数レコード追加クエリの構文で示したように SELECT...FROM 句によるクエリを使用します。この場合は、引数 *target* テーブルに追加するフィールドを SELECT 句で指定します。


            *source* または *target* テーブルでは、テーブルまたはクエリを指定できます。クエリを指定すると、Microsoft Access データベース エンジンは、クエリで指定されたすべてのテーブルにレコードを追加します。

INSERT INTO ステートメントは省略可能ですが、使用する場合 [SELECT](select-statement-microsoft-access-sql.md) ステートメントよりも前に記述します。

レコードの追加先のテーブルに主キーがある場合、その主キー フィールドには必ず **Null** 値以外の一意な値を追加するようにしてください。この条件が満たされない場合、Microsoft Access データベース エンジンはレコードを追加しません。

AutoNumber フィールドがあるレコードをテーブルに追加するときに、追加したレコードの番号を再割り当てしたい場合、クエリには AutoNumber フィールドは入れないでください。AutoNumber フィールドは、フィールドの元の値を維持したい場合のみ含めるようにしてください。

IN 句を使用し、別のデータベースのテーブルにレコードを追加してください。

新しいテーブルを作成する場合は、INSERT INTO ステートメントではなく、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントを使用してテーブル作成クエリを作成してください。

追加クエリを実行する前にどのレコードが追加されるかをあらかじめ確認する場合は、同じ抽出条件の選択クエリを実行してその結果を確認してください。

追加クエリは、1 つ以上のテーブルから別のテーブルにレコードをコピーします。追加するレコードを含むテーブルは、追加クエリの影響は受けません。

別のテーブルから既存のレコードを追加する代わりに、VALUES 句を使用して 1 つの新しいレコードに各フィールドの値を指定できます。フィールド一覧を省略した場合、VALUES 句にはテーブル内のすべてのフィールドの値を含める必要があります。そうしないと、INSERT 操作は失敗します。作成するそれぞれの追加レコードには、VALUES 句がある追加の INSERT INTO ステートメントを使用します。

[UtterAccess](https://www.utteraccess.com) コミュニティで**提供されるリンク**。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [INSERT/UPDATE ステートメントのための連続番号を生成](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [SQL から VBA のフォーマッタ](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a>例

次の例では、仮想の New Customers テーブルのすべてのレコードを選択し、それを Customers テーブルに追加します。列を個別に指定しない場合、SELECT テーブルの列名が INSERT INTO テーブルの列名と厳密に一致する必要があります。

```vb
    Sub InsertIntoX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all records in the New Customers table  
        ' and add them to the Customers table. 
        dbs.Execute " INSERT INTO Customers " _ 
            & "SELECT * " _ 
            & "FROM [New Customers];" 
             
        dbs.Close 
     
    End Sub
```

<br/>

次の使用例では、Employees テーブルに新しいレコードを作成します。

```vb
    Sub InsertIntoX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a new record in the Employees table. The  
        ' first name is Harry, the last name is Washington,  
        ' and the job title is Trainee. 
        dbs.Execute " INSERT INTO Employees " _ 
            & "(FirstName,LastName, Title) VALUES " _ 
            & "('Harry', 'Washington', 'Trainee');" 
             
        dbs.Close 
     
    End Sub 
```

