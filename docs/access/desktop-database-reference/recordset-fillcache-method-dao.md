---
title: Recordset メソッド (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ef268a821d65732e0a54776872387f62c67e999
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300519"
---
# <a name="recordsetfillcache-method-dao"></a>Recordset メソッド (DAO)

**適用先:** Access 2013、Office 2013

Microsoft Access データベース エンジンに接続されている ODBC データ ソースからのデータを格納する、 **Recordset** オブジェクト用のローカル キャッシュの全体または一部を埋めます (Microsoft Access データベース エンジンに接続された ODBC データベースのみ)。

## <a name="syntax"></a>構文

*式*。FillCache (***Rows***、 ***startbookmark***)

*式***Recordset**オブジェクトを表す変数を取得します。

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
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>キャッシュに格納する行の数を指定する、サブタイプが整数型 (<strong>Integer</strong>) のバリアント型 (<strong>Variant</strong>) の値です。 この引数を省略すると、値は<strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong>プロパティの設定によって決まります。</p></td>
</tr>
<tr class="even">
<td><p><em>StartBookmark</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>ブックマークを指定する、サブタイプが文字列型 (<strong>String</strong>) のバリアント型 (<strong>Variant</strong>) の値です。 このブックマークで示されたレコードを始点としてキャッシュが埋められます。 この引数を省略すると、 <strong><a href="recordset-cachestart-property-dao.md">cachestart</a></strong>プロパティによって示されたレコードから、キャッシュに格納されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

キャッシュを使用すると、リモート サーバーからデータを取得するアプリケーションのパフォーマンスが向上します。キャッシュは、直近に取得されたデータを保持するローカル メモリ内の領域で、アプリケーションの実行中にそのデータが再び要求されることを想定したものです。ユーザーがデータを要求すると、Microsoft Access データベース エンジンは、サーバーからそのデータを取得するのではなく、まずキャッシュにそのデータが保持されているかどうかを確認します。これは、前者の方法では時間がかかるからです。キャッシュには、ODBC データ ソース以外のデータは保存されません。

**FillCache** メソッドを使用すると、レコードの取得によってキャッシュが埋まるまで待たなくても、いつでも明示的にキャッシュを埋めることができます。 **FillCache** では、一度に 1 レコードずつではなく、複数のレコードが取得されるため、キャッシュをより迅速に埋めることができます。たとえば、レコードを画面いっぱいに表示している場合、アプリケーションでは、 **FillCache** を使用して、次に表示する画面いっぱいのレコードが取得されます。

**Recordset** オブジェクトを使用してアクセスする Microsoft Access データベース エンジンに接続されたすべての ODBC データ ソースには、ローカル キャッシュを割り当てることができます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、 **Recordset** の **CacheSize** プロパティと **CacheStart** プロパティを設定します。

rows および startbookmark では、 **CacheSize**プロパティと**cachestart**プロパティで指定されたレコード範囲の一部または全体の外側にある範囲のレコードが作成される場合、この範囲外の recordset の部分は無視され、読み込まれません。をキャッシュに入れます。

**FillCache** によって要求されたレコード数が、リモート データ ソースに残っているレコード数を上回っている場合、Microsoft Access データベース エンジンは、残っているレコードのみを取得します。この場合、エラーは発生しません。

> [!NOTE]
> - キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。
> - **FillCache** では、まだキャッシュされていないレコードだけが取得されます。キャッシュされたすべてのデータを強制的に更新するには、 **Recordset** の **CacheSize** プロパティを 0 に設定し、最初に要求したキャッシュのサイズにリセットしてから、 **FillCache** を使用します。

## <a name="example"></a>例

次の例では、 **CreateTableDef** メソッドと **FillCache** メソッド、および **CacheSize**、 **CacheStart**、 **SourceTableName** の各プロパティを使用して、リンクされたテーブルのレコードを 2 回列挙します。その後、50 レコードのキャッシュを使用してレコードを 2 回列挙します。さらに、リンクされたテーブルの処理にキャッシュを使用しなかった場合と使用した場合のパフォーマンス統計を表示します。

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset 
       Dim sngStart As Single 
       Dim sngEnd As Single 
       Dim sngNoCache As Single 
       Dim sngCache As Single 
       Dim intLoop As Integer 
       Dim strTemp As String 
       Dim intRecords As Integer 
     
       ' Open a database to which a linked table can be  
       ' appended. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a linked table that connects to a Microsoft SQL 
       ' Server database. 
       Set tdfRoyalties = _ 
          dbsCurrent.CreateTableDef("Royalties") 
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       tdfRoyalties.Connect = _ 
          "ODBC;DATABASE=pubs;DSN=Publishers" 
       tdfRoyalties.SourceTableName = "roysched" 
       dbsCurrent.TableDefs.Append tdfRoyalties 
       Set rstRemote = _ 
          dbsCurrent.OpenRecordset("Royalties") 
     
       With rstRemote 
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          sngStart = Timer 
     
          For intLoop = 1 To 2 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                .MoveNext 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngNoCache = sngEnd - sngStart 
     
          ' Cache the first 50 records. 
          .MoveFirst 
          .CacheSize = 50 
          .FillCache 
          sngStart = Timer 
     
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          For intLoop = 1 To 2 
             intRecords = 0 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                ' Count the records. If the end of the 
                ' cache is reached, reset the cache to the 
                ' next 50 records. 
                intRecords = intRecords + 1 
                .MoveNext 
                If intRecords Mod 50 = 0 Then 
                   .CacheStart = .Bookmark 
                   .FillCache 
                End If 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngCache = sngEnd - sngStart 
     
          ' Display performance results. 
          MsgBox "Caching Performance Results:" & vbCr & _ 
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```
