---
title: Recordset2 メソッド (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 2098df82375ac47b7d5abe0bd63b0af2bb29ba40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309703"
---
# <a name="recordset2fillcache-method-dao"></a><span data-ttu-id="364d7-102">Recordset2 メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="364d7-102">Recordset2.FillCache method (DAO)</span></span>

<span data-ttu-id="364d7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="364d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="364d7-104">Microsoft Access データベース エンジンに接続されている ODBC データ ソースからのデータを格納する、 **Recordset** オブジェクト用のローカル キャッシュの全体または一部を埋めます (Microsoft Access データベース エンジンに接続された ODBC データベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="364d7-104">Fills all or a part of a local cache for a **Recordset** object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span>

## <a name="syntax"></a><span data-ttu-id="364d7-105">構文</span><span class="sxs-lookup"><span data-stu-id="364d7-105">Syntax</span></span>

<span data-ttu-id="364d7-106">*式*。FillCache (***Rows***、 ***startbookmark***)</span><span class="sxs-lookup"><span data-stu-id="364d7-106">*expression* .FillCache(***Rows***, ***StartBookmark***)</span></span>

<span data-ttu-id="364d7-107">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="364d7-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="364d7-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="364d7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="364d7-109">名前</span><span class="sxs-lookup"><span data-stu-id="364d7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="364d7-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="364d7-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="364d7-111">データ型</span><span class="sxs-lookup"><span data-stu-id="364d7-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="364d7-112">説明</span><span class="sxs-lookup"><span data-stu-id="364d7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="364d7-113"><em>Rows</em></span><span class="sxs-lookup"><span data-stu-id="364d7-113"><em>Rows</em></span></span></p></td>
<td><p><span data-ttu-id="364d7-114">Optional</span><span class="sxs-lookup"><span data-stu-id="364d7-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="364d7-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="364d7-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="364d7-116">キャッシュに格納する行の数を指定する、サブタイプが整数型 (<strong>Integer</strong>) のバリアント型 (<strong>Variant</strong>) の値です。</span><span class="sxs-lookup"><span data-stu-id="364d7-116">A <strong>Variant</strong> (<strong>Integer</strong> subtype) that specifies the number of rows to store in the cache.</span></span> <span data-ttu-id="364d7-117">この引数を省略すると、値は<strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong>プロパティの設定によって決まります。</span><span class="sxs-lookup"><span data-stu-id="364d7-117">If you omit this argument, the value is determined by the <strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong> property setting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="364d7-118"><em>StartBookmark</em></span><span class="sxs-lookup"><span data-stu-id="364d7-118"><em>StartBookmark</em></span></span></p></td>
<td><p><span data-ttu-id="364d7-119">Optional</span><span class="sxs-lookup"><span data-stu-id="364d7-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="364d7-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="364d7-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="364d7-121">ブックマークを指定する、サブタイプが文字列型 (<strong>String</strong>) のバリアント型 (<strong>Variant</strong>) の値です。</span><span class="sxs-lookup"><span data-stu-id="364d7-121">A <strong>Variant</strong> (<strong>String</strong> subtype) that specifies a bookmark.</span></span> <span data-ttu-id="364d7-122">このブックマークで示されたレコードを始点としてキャッシュが埋められます。</span><span class="sxs-lookup"><span data-stu-id="364d7-122">The cache is filled starting from the record indicated by this bookmark.</span></span> <span data-ttu-id="364d7-123">この引数を省略すると、 <strong><a href="recordset2-cachestart-property-dao.md">cachestart</a></strong>プロパティによって示されたレコードから、キャッシュに格納されます。</span><span class="sxs-lookup"><span data-stu-id="364d7-123">If you omit this argument, the cache is filled starting from the record indicated by the <strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="364d7-124">注釈</span><span class="sxs-lookup"><span data-stu-id="364d7-124">Remarks</span></span>

<span data-ttu-id="364d7-p103">キャッシュを使用すると、リモート サーバーからデータを取得するアプリケーションのパフォーマンスが向上します。キャッシュは、直近に取得されたデータを保持するローカル メモリ内の領域で、アプリケーションの実行中にそのデータが再び要求されることを想定したものです。ユーザーがデータを要求すると、Microsoft Access データベース エンジンは、サーバーからそのデータを取得するのではなく、まずキャッシュにそのデータが保持されているかどうかを確認します。これは、前者の方法では時間がかかるからです。キャッシュには、ODBC データ ソース以外のデータは保存されません。</span><span class="sxs-lookup"><span data-stu-id="364d7-p103">Caching improves the performance of an application that retrieves data from a remote server. A cache is space in local memory that holds the data most recently retrieved from the server; this assumes that the data will probably be requested again while the application is running. When a user requests data, the Microsoft Access database engine checks the cache for the data first rather than retrieving it from the server, which takes more time. The cache doesn't save data that doesn't come from an ODBC data source.</span></span>

<span data-ttu-id="364d7-p104">**FillCache** メソッドを使用すると、レコードの取得によってキャッシュが埋まるまで待たなくても、いつでも明示的にキャッシュを埋めることができます。 **FillCache** では、一度に 1 レコードずつではなく、複数のレコードが取得されるため、キャッシュをより迅速に埋めることができます。たとえば、レコードを画面いっぱいに表示している場合、アプリケーションでは、 **FillCache** を使用して、次に表示する画面いっぱいのレコードが取得されます。</span><span class="sxs-lookup"><span data-stu-id="364d7-p104">Rather than waiting for the cache to be filled with records as they are retrieved, you can use the **FillCache** method to explicitly fill the cache at any time. This is a faster way to fill the cache because **FillCache** retrieves several records at once instead of one at a time. For example, while you view each screenful of records, your application uses **FillCache** to retrieve the next screenful of records for viewing.</span></span>

<span data-ttu-id="364d7-p105">**Recordset** オブジェクトを使用してアクセスする Microsoft Access データベース エンジンに接続されたすべての ODBC データ ソースには、ローカル キャッシュを割り当てることができます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、 **Recordset** の **CacheSize** プロパティと **CacheStart** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="364d7-p105">Any Microsoft Access database engine-connected ODBC data source that you access with **Recordset** objects can have a local cache. To create the cache, open a **Recordset** object from the remote data source, and then set the **CacheSize** and **CacheStart** properties of the **Recordset**.</span></span>

<span data-ttu-id="364d7-134">rows および startbookmark では、 **CacheSize**プロパティと**cachestart**プロパティで指定されたレコード範囲の一部または全体の外側にある範囲のレコードが作成される場合、この範囲外の recordset の部分は無視され、読み込まれません。をキャッシュに入れます。</span><span class="sxs-lookup"><span data-stu-id="364d7-134">If rows and startbookmark create a range of records that is partially or entirely outside the range of records specified by the **CacheSize** and **CacheStart** properties, the portion of the recordset outside this range is ignored and will not be loaded into the cache.</span></span>

<span data-ttu-id="364d7-135">**FillCache** によって要求されたレコード数が、リモート データ ソースに残っているレコード数を上回っている場合、Microsoft Access データベース エンジンは、残っているレコードのみを取得します。この場合、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="364d7-135">If **FillCache** requests more records than the number remaining in the remote data source, the Microsoft Access database engine retrieves only the remaining records, and no error occurs.</span></span>

> [!NOTE]
> - <span data-ttu-id="364d7-136">キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。</span><span class="sxs-lookup"><span data-stu-id="364d7-136">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>
> - <span data-ttu-id="364d7-p106">**FillCache** では、まだキャッシュされていないレコードだけが取得されます。キャッシュされたすべてのデータを強制的に更新するには、 **Recordset** の **CacheSize** プロパティを 0 に設定し、最初に要求したキャッシュのサイズにリセットしてから、 **FillCache** を使用します。</span><span class="sxs-lookup"><span data-stu-id="364d7-p106">**FillCache** only retrieves records not already cached. To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.</span></span>

## <a name="example"></a><span data-ttu-id="364d7-139">例</span><span class="sxs-lookup"><span data-stu-id="364d7-139">Example</span></span>

<span data-ttu-id="364d7-p107">次の例では、 **CreateTableDef** メソッドと **FillCache** メソッド、および **CacheSize**、 **CacheStart**、 **SourceTableName** の各プロパティを使用して、リンクされたテーブルのレコードを 2 回列挙します。その後、50 レコードのキャッシュを使用してレコードを 2 回列挙します。さらに、リンクされたテーブルの処理にキャッシュを使用しなかった場合と使用した場合のパフォーマンス統計を表示します。</span><span class="sxs-lookup"><span data-stu-id="364d7-p107">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
