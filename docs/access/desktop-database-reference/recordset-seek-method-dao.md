---
title: Recordset.Seek メソッド (DAO)
TOCTitle: Seek Method
ms:assetid: ef83d909-c962-b016-7d33-36eacdc25c2c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836416(v=office.15)
ms:contentKeyID: 48548585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053061
f1_categories:
- Office.Version=v15
ms.localizationpriority: high
ms.openlocfilehash: 5942da3b0ea4ab2b2df7a4bbf55555378f8b4bb3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585432"
---
# <a name="recordsetseek-method-dao"></a>Recordset.Seek メソッド (DAO)

**適用先:** Access 2013、Office 2013

インデックス付きのテーブル タイプの **Recordset** オブジェクトで、現在のインデックスの指定された抽出条件を満たすレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*expression* .Seek(***Comparison** _, _*_Key1_*_, _*_Key2_*_, _*_Key3_*_, _*_Key4_*_, _*_Key5_*_, _*_Key6_*_, _*_Key7_*_, _*_Key8_*_, _*_Key9_*_, _*_Key10_*_, _*_Key11_*_, _*_Key12_*_, _*_Key13_**)

*expression*: **Recordset** オブジェクトを表す変数。

## <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須かどうか</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>比較</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>&lt;、&lt;=、=、&gt;=、&gt; のうちいずれかの文字列式です。</p></td>
</tr>
<tr class="even">
<td><p><em>Key1, Key2...Key13</em></p></td>
<td><p>必須</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Recordset</strong> オブジェクトの <strong>Index</strong> プロパティの設定で指定された現在のインデックスのフィールドに対応する 1 つ以上の値です。引数 key は最大 13 個まで使用できます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**Seek** を使用する前に、**Index** プロパティで現在のインデックスを設定しておく必要があります。インデックスが一意でないキー フィールドを指している場合、**Seek** は抽出条件を満たす最初のレコードを返します。

**Seek** メソッドは、指定されたキー フィールドを検索し、引数 comparison および key1 で指定された条件を満たす最初のレコードを返します。レコードを検出すると、そのレコードをカレント レコードにし、**NoMatch** プロパティを **False** に設定します。**Seek** メソッドで一致するレコードが見つからなかった場合は、**NoMatch** プロパティが **True** に設定され、カレント レコードは未定義となります。

比較が、等しい (=)、以上 (\>=)、またはより大きい (\>)である場合、**Seek** はインデックスの先頭から始まり、末尾に向かって検索を進めます。

comparison が、より小さい (\<)、または以下 (\<=) である場合、**Seek** はインデックスの末尾から始まり、先頭に向かって検索を進めます。しかし、インデックスの末尾に重複するインデックスのエントリがある場合、**Seek** は重複するエントリのうち任意のエントリから始まり、先頭に向かって検索を進めます。

インデックスで定義されているすべてのフィールドには、値を指定する必要があります。複数列のインデックスを指定して **Seek** を使用するときに、インデックスのすべてのフィールドに comparison の値を指定しない場合は、comparison に等値演算子 (=) を使用できません。これは、抽出条件フィールドの一部 (key2、key3 など) に、既定で Null が設定され、これが一致することはないと考えられるからです。このため、等値演算子が正しく機能するのは、検索対象以外のすべてのキーが **null** であるレコードが存在する場合だけです。代わりに、以上演算子 (\>=) を使用することをお勧めします。

引数 key1 のフィールドのデータ型は、現在のインデックスの対応するフィールドのデータ型と同じである必要があります。たとえば、現在のインデックスが数値フィールド (従業員 ID など) を参照している場合、key1 は数字である必要があります。同様に、現在のインデックスがテキスト フィールド (姓など) を参照している場合、key1 は文字列である必要があります。

**Seek** を使用するときは、カレント レコードが設定されている必要はありません。

**[Indexes](indexes-collection-dao.md)** コレクションを使用すると、既存のインデックスを列挙できます。

ダイナセット タイプまたはスナップショット タイプの **Recordset** で、既存のインデックスでは対応できない特定の条件を満たすレコードを検索するには、 **[Find](recordset-findfirst-method-dao.md)** メソッドを使用します。特定の条件を満たすレコードだけでなく、すべてのレコードを対象にするには、 **[Move](recordset-movefirst-method-dao.md)** メソッドを使用してレコード間を移動します。

リンク テーブルはテーブル タイプの **Recordset** オブジェクトとして開くことができないため、 **Seek** メソッドはリンク テーブルに対して使用できません。しかし、 **[OpenDatabase](dbengine-opendatabase-method-dao.md)** メソッドを使用してインストール可能な ISAM (ODBC でない) データベースを直接開いた場合は、そのデータベース内のテーブルに対して **Seek** を使用できます。

## <a name="example"></a>例

この例では、**Seek** メソッドを使用して、ユーザーが ID 番号に基づき製品を検索できるようにする方法を示します。

```vb
    Sub SeekX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim intFirst As Integer 
       Dim intLast As Integer 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' You must open a table-type Recordset to use an index,  
       ' and hence the Seek method. 
       Set rstProducts = _ 
          dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
       With rstProducts 
          ' Set the index. 
          .Index = "PrimaryKey" 
     
          ' Get the lowest and highest product IDs. 
          .MoveLast 
          intLast = !ProductID 
          .MoveFirst 
          intFirst = !ProductID 
     
          Do While True 
             ' Display current record information and ask user  
             ' for ID number. 
             strMessage = "Product ID: " & !ProductID & vbCr & _ 
                "Name: " & !ProductName & vbCr & vbCr & _ 
                "Enter a product ID between " & intFirst & _ 
                " and " & intLast & "." 
             strSeek = InputBox(strMessage) 
     
             If strSeek = "" Then Exit Do 
     
             ' Store current bookmark in case the Seek fails. 
             varBookmark = .Bookmark 
     
             .Seek "=", Val(strSeek) 
     
             ' Return to the current record if the Seek fails. 
             If .NoMatch Then 
                MsgBox "ID not found!" 
                .Bookmark = varBookmark 
             End If 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
```

<br/>

次の例では、 **NoMatch** プロパティを使用して **Seek** および **FindFirst** が成功したかどうか確認し、成功しなかった場合は適切なフィードバックを表示します。このプロシージャを実行するには、SeekMatch プロシージャと FindMatch プロシージャが必要です。

```vb
    Sub NoMatchX() 
     
       Dim dbsNorthwind As Database 
       Dim rstProducts As Recordset 
       Dim rstCustomers As Recordset 
       Dim strMessage As String 
       Dim strSeek As String 
       Dim strCountry As String 
       Dim varBookmark As Variant 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' Default is dbOpenTable; required if Index property will  
       ' be used. 
       Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
       With rstProducts 
          .Index = "PrimaryKey" 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with Seek method" & vbCr & _ 
                "Product ID: " & !ProductID & vbCr & _ 
                "Product Name: " & !ProductName & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter a product ID." 
             strSeek = InputBox(strMessage) 
             If strSeek = "" Then Exit Do 
     
             ' Call procedure that seeks for a record based on  
             ' the ID number supplied by the user. 
             SeekMatch rstProducts, Val(strSeek) 
          Loop 
     
          .Close 
       End With 
     
       Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
          "SELECT CompanyName, Country FROM Customers " & _ 
          "ORDER BY CompanyName", dbOpenSnapshot) 
     
       With rstCustomers 
     
          Do While True 
             ' Show current record information; ask user for  
             ' input. 
             strMessage = "NoMatch with FindFirst method" & _ 
                vbCr & "Customer Name: " & !CompanyName & _ 
                vbCr & "Country: " & !Country & vbCr & _ 
                "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
                "Enter country on which to search." 
             strCountry = Trim(InputBox(strMessage)) 
             If strCountry = "" Then Exit Do 
     
             ' Call procedure that finds a record based on  
             ' the country name supplied by the user. 
             FindMatch rstCustomers, _ 
                "Country = '" & strCountry & "'" 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
       intSeek As Integer) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .Seek "=", intSeek 
     
          ' If Seek method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
       strFind As String) 
     
       Dim varBookmark As Variant 
       Dim strMessage As String 
     
       With rstTemp 
          ' Store current record location. 
          varBookmark = .Bookmark 
          .FindFirst strFind 
     
          ' If Find method fails, notify user and return to the  
          ' last current record. 
          If .NoMatch Then 
             strMessage = _ 
                "Not found! Returning to current record." & _ 
                vbCr & vbCr & "NoMatch = " & .NoMatch 
             MsgBox strMessage 
             .Bookmark = varBookmark 
          End If 
     
       End With 
     
    End Sub 
```

<br/>

次の例は、Seek メソッドを使用して、リンクしたテーブル内のレコードを見つける方法を示します。

**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。

```vb
    Sub TestSeek()
        ' Get the path to the external database that contains
        ' the tblCustomers table we're going to search.
        Dim strMyExternalDatabase
        Dim dbs    As DAO.Database
        Dim dbsExt As DAO.Database
        Dim rst    As DAO.Recordset
        Dim tdf    As DAO.TableDef
        
        Set dbs = CurrentDb()
        Set tdf = dbs.TableDefs("tblCustomers")
        strMyExternalDatabase = Mid(tdf.Connect, 11)
        
        'Open the database that contains the table that is linked
        Set dbsExt = OpenDatabase(strMyExternalDatabase)
        
        'Open a table-type recordset against the external table
        Set rst = dbsExt.OpenRecordset("tblCustomers", dbOpenTable)
        
        'Specify which index to search on
        rst.Index = "PrimaryKey"
        
        'Specify the criteria
        rst.Seek "=", 123
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
        Else
            MsgBox "Customer name: " & rst!CustName
        End If
        
        rst.Close
        dbs.Close
        dbsExt.Close
        Set rst = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
        
        
    End Sub
```
