---
title: Recordset2.FillCache メソッド (DAO)
TOCTitle: FillCache Method
ms:assetid: 28a70997-a8d4-73e6-171a-61286e3d3485
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192007(v=office.15)
ms:contentKeyID: 48543864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052942
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 279f0f759bc54d4cb4a6c02f0fa61070fe79fbc0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478410"
---
# <a name="recordset2fillcache-method-dao"></a>Recordset2.FillCache メソッド (DAO)


**適用されます**Access 2013 |。Office 2013

Microsoft Access データベース エンジンに接続している ODBC データ ソースのデータを格納している **Recordset** オブジェクトについて、ローカル キャッシュの全部または一部にデータを格納します (Microsoft Access データベース エンジンに接続している ODBC データベースのみ)。

## <a name="syntax"></a>構文

*式*です。FillCache (***行***、 ***StartBookmark***)

*式***Recordset2**オブジェクトを表す変数です。

### <a name="parameters"></a>パラメーター

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
<td><p>行</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>キャッシュに格納する行数を表す、サブタイプが整数型 (<strong>Integer</strong>) であるバリアント型 (<strong>Variant</strong>) の値。この引数を省略した場合、<strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> プロパティの設定値によって値が指定されます。</p></td>
</tr>
<tr class="even">
<td><p>StartBookmark</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>ブックマークを表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。このブックマークで示されたレコードから、キャッシュへの読み込みが開始されます。この引数を省略した場合、<strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> プロパティによって示されたレコードから、キャッシュへの読み込みが開始されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

キャッシュを使用すると、リモート サーバーからデータを取得するアプリケーションのパフォーマンスが向上します。キャッシュは、サーバーから最近取得したデータを格納しておくローカル メモリ内の領域ですが、これはアプリケーションの実行中にそのデータが再び要求されるであろうということを前提としています。サーバーからデータを取得するにはキャッシュ内のデータを使用するよりも時間がかかるため、ユーザーがデータが要求すると、そのデータがキャッシュにないかが最初に調べられます。ODBC データベース ソース以外からのデータはキャッシュに保存されません。

取得されたレコードがそのつどキャッシュに格納されるのを待つ代わりに、任意の時点で **FillCache** メソッドを使用して、明示的にキャッシュに格納できます。 **FillCache** を使用すると、レコードが 1 つずつではなく、一度にまとめて格納されるため、処理速度が向上します。たとえば、アプリケーションでは、画面にレコードを表示している間に、 **FillCache** を使用して次に表示する画面のレコードを取得します。

Microsoft Access データベース エンジンに接続している ODBC データ ソースに **Recordset** オブジェクトを使用してアクセスする場合は、ローカル キャッシュを設定できます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、次に **Recordset** の **CacheSize** プロパティと **CacheStart** プロパティを設定します。

行および startbookmark は、レコードの一部がはみ出しているのか、 **CacheSize**プロパティと**CacheStart**プロパティで指定されたレコードの範囲の完全に外側の範囲を作成する場合、この範囲外のレコード セットの一部は無視され、読み込まれなくなりますキャッシュします。

**FillCache** で要求したレコードの数がリモート データ ソースに残っているレコードの数よりも多い場合は、残りのレコードのみが取得され、エラーは発生しません。


> [!NOTE]
> <UL>
> <LI>
> <P>キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。</P>
> <LI>
> <P><STRONG>FillCache</STRONG> では、まだキャッシュされていないレコードのみが取得されます。キャッシュされたすべてのデータの更新を強制実行するには、 <STRONG>Recordset</STRONG> の <STRONG>CacheSize</STRONG> をいったん 0 に設定し、当初に要求したキャッシュのサイズに再び設定してから、 <STRONG>FillCache</STRONG> を使用します。</P></LI></UL>



## <a name="example"></a>例

次の使用例では、 **CreateTableDef** メソッドと **FillCache** メソッド、および **CacheSize**、 **CacheStart**、 **SourceTableName** の各プロパティを使用して、リンク テーブルのレコードを 2 回列挙します。次に、50 件のレコードをキャッシュして、すべてのレコードを 2 回列挙します。最後に、リンク テーブルを使用して、キャッシュされていない実行とキャッシュされた実行のパフォーマンス統計を表示します。

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset2 
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
