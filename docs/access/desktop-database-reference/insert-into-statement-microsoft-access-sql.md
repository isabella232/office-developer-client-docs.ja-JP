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
ms.openlocfilehash: c20701e9863d72a9308679965425b74c9f9818ac
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937639"
---
# <a name="insert-into-statement-microsoft-access-sql"></a>INSERT INTO ステートメント (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

テーブルに 1 つまたは複数のレコードを追加します。追加クエリとも呼ばれます。

## <a name="syntax"></a>構文

### <a name="multiple-record-append-query"></a>複数レコード追加クエリ

INSERT INTO*ターゲット* \[(*フィールド 1*\[、*フィールド 2*\[、.\] \])\] \[ *Externaldatabase*で\]を選択して\[*ソース*です。\]*フィールド 1*\[、*フィールド 2*\[をしています.\] *Tableexpression*から

### <a name="single-record-append-query"></a>単一レコード追加クエリ

INSERT INTO*ターゲット* \[(*フィールド 1*\[、*フィールド 2*\[、.\] \])\]の値 (*値 1*\[、*値 2*\[、.\])

INSERT INTO ステートメントには、次の指定項目があります。

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
<td><p><em>target</em></p></td>
<td><p>レコードを追加するテーブルまたはクエリの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>field1</em>、<em>field2</em></p></td>
<td><p><em>ターゲット</em>の引数では、次の場合に、データを追加するフィールドの名前または<em>変換元</em>の引数を次の場合からのデータを取得するフィールドの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>externaldatabase</em></p></td>
<td><p>外部データベースのパス。パスの記述方法については、「<a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN 句</a>」を参照してください。  </p></td>
</tr>
<tr class="even">
<td><p><em>source</em></p></td>
<td><p>コピー元のレコードのあるテーブルまたはクエリの名前。</p></td>
</tr>
<tr class="odd">
<td><p><em>tableexpression</em></p></td>
<td><p>挿入するレコードのある 1 つ以上のテーブルの名前。単一のテーブル名、保存されたクエリ名、または <a href="inner-join-operation-microsoft-access-sql.md">INNER JOIN</a>、<a href="left-join-right-join-operations-microsoft-access-sql.md">LEFT JOIN</a>、<a href="left-join-right-join-operations-microsoft-access-sql.md">RIGHT JOIN</a> のいずれかの操作の結果としてできる複合テーブルを指定します。  </p></td>
</tr>
<tr class="even">
<td><p><em>value1</em>、<em>value2</em></p></td>
<td><p>新しいレコードの特定のフィールドに挿入する値。それぞれの値は、記述順にフィールドに挿入されます。つまり、引数 <em>value1</em> は新しいレコードの引数 <em>field1</em> に、引数 <em>value2</em> は引数 <em>value2</em> に挿入されます。値と値の間はコンマで区切り、テキスト フィールドの値は単一引用符 (') で囲みます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

INSERT INTO ステートメントで 1 つのレコードを追加するには、上記のように単一レコード追加クエリの構文を使用します。この場合は、レコードの各フィールドの名前と値を指定します。また、値を割り当てるフィールドと、そのフィールドに割り当てる値を指定します。指定していないフィールドには、既定値または **Null** 値が挿入されます。レコードはテーブルの末尾に追加されます。

また、INSERT INTO ステートメントを使用して、別のテーブルからレコードのセットを追加することもできます。 これには、上記の複数レコード追加クエリの構文で示したように SELECT...FROM 句によるクエリを使用します。 この例では、SELECT 句は、指定された*ターゲット*テーブルに追加するフィールドを指定します。

*ソース*または*ターゲット*テーブルには、テーブルまたはクエリを指定できます。 クエリを指定した場合、Microsoft Access データベース エンジンは、クエリで指定したすべてのテーブルにレコードを追加します。

INSERT INTO ステートメントは省略可能ですが、使用する場合 [SELECT](select-statement-microsoft-access-sql.md) ステートメントよりも前に記述します。

レコードの追加先のテーブルに主キーがある場合、その主キー フィールドには必ず **Null** 値以外の一意な値を追加するようにしてください。この条件が満たされない場合、Microsoft Access データベース エンジンはレコードを追加しません。

オートナンバ型 (AutoNumber) フィールドのあるテーブルにレコードを追加する場合、追加したレコードに新しく番号を割り当てる場合は、クエリにオートナンバ型 (AutoNumber) フィールドを含めないでください。既にこのフィールドに割り当てられている値をそのまま使用する場合は、クエリにオートナンバ型 (AutoNumber) フィールドを含めてください。

別のデータベースにあるテーブルにレコードを追加するには、IN 句を使用します。

新しいテーブルを作成する場合は、INSERT INTO ステートメントではなく、[SELECT...INTO](select-into-statement-microsoft-access-sql.md) ステートメントを使用してテーブル作成クエリを作成してください。

追加クエリを実行する前にどのレコードが追加されるかをあらかじめ確認する場合は、同じ抽出条件の選択クエリを実行してその結果を確認してください。

追加クエリを実行すると、1 つまたは複数のテーブルから他のテーブルにレコードがコピーされます。追加クエリを実行しても、レコードのコピー元のテーブルは変更されません。

別のテーブルからの既存のレコードを追加する代わりに、VALUES 句を使用して、各フィールドの値を指定した単一の新規レコードを追加することもできます。フィールド リストを省略する場合は、VALUES 句にはテーブルにあるすべてのフィールドの値を指定してください。すべてのフィールドの値を指定しないと、INSERT 操作は失敗します。VALUES 句を使用する INSERT INTO ステートメントは、追加するレコードの数だけ記述する必要があります。

**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。 UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。

- [INSERT/UPDATE ステートメントのための連続番号を生成](https://www.utteraccess.com/forum/generating-sequential-num-t446039.html)

- [SQL から VBA のフォーマッタ](https://www.utteraccess.com/forum/sql-vba-formatter-t1165308.html)

## <a name="example"></a>使用例

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

