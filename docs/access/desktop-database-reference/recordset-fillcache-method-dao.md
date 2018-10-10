---
title: Recordset.FillCache メソッド (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fb7a662a061a7e98d3782d0c42badeda77ab3a8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478221"
---
# <a name="recordsetfillcache-method-dao"></a><span data-ttu-id="c127d-102">Recordset.FillCache メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="c127d-102">Recordset.FillCache Method (DAO)</span></span>


<span data-ttu-id="c127d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c127d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c127d-104">Microsoft Access データベース エンジンに接続している ODBC データ ソースのデータを格納している **Recordset** オブジェクトについて、ローカル キャッシュの全部または一部にデータを格納します (Microsoft Access データベース エンジンに接続している ODBC データベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c127d-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c127d-105">構文</span><span class="sxs-lookup"><span data-stu-id="c127d-105">Syntax</span></span>

<span data-ttu-id="c127d-106">*式*です。FillCache (***行***、 ***StartBookmark***)</span><span class="sxs-lookup"><span data-stu-id="c127d-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="c127d-107">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c127d-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="c127d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c127d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c127d-109">名前</span><span class="sxs-lookup"><span data-stu-id="c127d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c127d-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="c127d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="c127d-111">データ型</span><span class="sxs-lookup"><span data-stu-id="c127d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="c127d-112">説明</span><span class="sxs-lookup"><span data-stu-id="c127d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c127d-113">行</span><span class="sxs-lookup"><span data-stu-id="c127d-113">Rows</span></span></p></td>
<td><p><span data-ttu-id="c127d-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="c127d-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="c127d-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="c127d-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c127d-p101">キャッシュに格納する行数を表す、サブタイプが整数型 (<strong>Integer</strong>) であるバリアント型 (<strong>Variant</strong>) の値。この引数を省略した場合、<strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> プロパティの設定値によって値が指定されます。</span><span class="sxs-lookup"><span data-stu-id="c127d-p101">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache. If you omit this argument, the value is determined by the <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c127d-118">StartBookmark</span><span class="sxs-lookup"><span data-stu-id="c127d-118">StartBookmark</span></span></p></td>
<td><p><span data-ttu-id="c127d-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="c127d-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="c127d-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="c127d-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c127d-p102">ブックマークを表す、サブタイプが文字列型 (<strong>String</strong>) であるバリアント型 (<strong>Variant</strong>) の値。このブックマークで示されたレコードから、キャッシュへの読み込みが開始されます。この引数を省略した場合、<strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> プロパティによって示されたレコードから、キャッシュへの読み込みが開始されます。</span><span class="sxs-lookup"><span data-stu-id="c127d-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark. The cache is filled starting from the record indicated by this bookmark. If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c127d-124">注釈</span><span class="sxs-lookup"><span data-stu-id="c127d-124">Remarks</span></span>

<span data-ttu-id="c127d-p103">キャッシュを使用すると、リモート サーバーからデータを取得するアプリケーションのパフォーマンスが向上します。キャッシュは、サーバーから最近取得したデータを格納しておくローカル メモリ内の領域ですが、これはアプリケーションの実行中にそのデータが再び要求されるであろうということを前提としています。サーバーからデータを取得するにはキャッシュ内のデータを使用するよりも時間がかかるため、ユーザーがデータが要求すると、そのデータがキャッシュにないかが最初に調べられます。ODBC データベース ソース以外からのデータはキャッシュに保存されません。</span><span class="sxs-lookup"><span data-stu-id="c127d-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="c127d-p104">取得されたレコードがそのつどキャッシュに格納されるのを待つ代わりに、任意の時点で **FillCache** メソッドを使用して、明示的にキャッシュに格納できます。 **FillCache** を使用すると、レコードが 1 つずつではなく、一度にまとめて格納されるため、処理速度が向上します。たとえば、アプリケーションでは、画面にレコードを表示している間に、 **FillCache** を使用して次に表示する画面のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="c127d-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="c127d-p105">Microsoft Access データベース エンジンに接続している ODBC データ ソースに **Recordset** オブジェクトを使用してアクセスする場合は、ローカル キャッシュを設定できます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、次に **Recordset** の **CacheSize** プロパティと **CacheStart** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="c127d-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="c127d-134">行および startbookmark は、レコードの一部がはみ出しているのか、 **CacheSize**プロパティと**CacheStart**プロパティで指定されたレコードの範囲の完全に外側の範囲を作成する場合、この範囲外のレコード セットの一部は無視され、読み込まれなくなりますキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="c127d-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="c127d-135">**FillCache** で要求したレコードの数がリモート データ ソースに残っているレコードの数よりも多い場合は、残りのレコードのみが取得され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="c127d-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="c127d-136">キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。</span><span class="sxs-lookup"><span data-stu-id="c127d-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span></P>
> <LI>
> <P><span data-ttu-id="c127d-p106"><STRONG>FillCache</STRONG> では、まだキャッシュされていないレコードのみが取得されます。キャッシュされたすべてのデータの更新を強制実行するには、 <STRONG>Recordset</STRONG> の <STRONG>CacheSize</STRONG> をいったん 0 に設定し、当初に要求したキャッシュのサイズに再び設定してから、 <STRONG>FillCache</STRONG> を使用します。</span><span class="sxs-lookup"><span data-stu-id="c127d-p106"><STRONG>FillCache</STRONG> only retrieves records not already cached. To force an update of all the cached data, set the <STRONG>CacheSize</STRONG> property of the <STRONG>Recordset</STRONG> to 0, reset it to the size of the cache you originally requested, and then use <STRONG>FillCache</STRONG>.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="c127d-139">例</span><span class="sxs-lookup"><span data-stu-id="c127d-139">Example</span></span>

<span data-ttu-id="c127d-p107">次の使用例では、 **CreateTableDef** メソッドと **FillCache** メソッド、および **CacheSize**、 **CacheStart**、 **SourceTableName** の各プロパティを使用して、リンク テーブルのレコードを 2 回列挙します。次に、50 件のレコードをキャッシュして、すべてのレコードを 2 回列挙します。最後に、リンク テーブルを使用して、キャッシュされていない実行とキャッシュされた実行のパフォーマンス統計を表示します。</span><span class="sxs-lookup"><span data-stu-id="c127d-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
