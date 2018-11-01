---
title: Recordset2.CacheSize プロパティ (DAO)
TOCTitle: CacheSize Property
ms:assetid: d8d195cc-6696-0583-31eb-b9988f8b7c6f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835090(v=office.15)
ms:contentKeyID: 48548042
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052927
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f314644d54c7a6361cf196f4e3c2a59df8af271d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872243"
---
# <a name="recordset2cachesize-property-dao"></a><span data-ttu-id="e4716-102">Recordset2.CacheSize プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="e4716-102">Recordset2.CacheSize Property (DAO)</span></span>


<span data-ttu-id="e4716-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e4716-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4716-p101">ローカル メモリにキャッシュされた ODBC データ ソースから取得したレコード数を設定または取得します。値の取得および設定が可能です。長整数型 ( **Long**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e4716-p101">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4716-106">構文</span><span class="sxs-lookup"><span data-stu-id="e4716-106">Syntax</span></span>

<span data-ttu-id="e4716-107">*式*です。CacheSize</span><span class="sxs-lookup"><span data-stu-id="e4716-107">*expression* .CacheSize</span></span>

<span data-ttu-id="e4716-108">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="e4716-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4716-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e4716-109">Remarks</span></span>

<span data-ttu-id="e4716-p102">**CacheSize** プロパティの値は 5 ～ 1200 の範囲内で、利用可能な空きメモリ以下である必要があります。一般的な値は 100 です。0 を設定すると、キャッシングがオフになります。</span><span class="sxs-lookup"><span data-stu-id="e4716-p102">The value of the **CacheSize** property must be between 5 and 1200, but not greater than available memory will allow. A typical value is 100. A setting of 0 turns off caching.</span></span>

<span data-ttu-id="e4716-p103">**Recordset** オブジェクトを使用してリモート サーバーからデータを取得する場合、データをキャッシュするとパフォーマンスが向上します。キャッシュとは、サーバーから最近取得したデータを保持するローカル メモリ内の領域で、アプリケーションの実行中にユーザーが再度同じデータを要求した場合に役に立ちます。ユーザーがデータを要求すると、Microsoft Access データベース エンジンでは、最初にキャッシュ内に要求されたデータがあるかどうかを確認し、より時間のかかるサーバーからの取得はキャッシュにデータがない場合に行われます。キャッシュに保存されるデータは、ODBC データ ソースのデータのみです。</span><span class="sxs-lookup"><span data-stu-id="e4716-p103">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="e4716-p104">リンク テーブルなどの Microsoft Access データベース エンジンに接続された ODBC データ ソースには、ローカル キャッシュを設定できます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、 **CacheSize** プロパティと **[CacheStart](recordset2-cachestart-property-dao.md)** プロパティを設定し、次に、 **[FillCache](recordset2-fillcache-method-dao.md)** メソッドを使用するか、 **Move** メソッドを使用してレコード間を移動します。</span><span class="sxs-lookup"><span data-stu-id="e4716-p104">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="e4716-p105">**CacheSize** プロパティは、アプリケーションが一度に処理できるレコード数に基づいて設定できます。たとえば、画面に表示するデータ ソースとして **Recordset** オブジェクトを使用している場合、その **CacheSize** プロパティを 20 に設定すると、一度に 20 レコード表示できます。</span><span class="sxs-lookup"><span data-stu-id="e4716-p105">You can base the **CacheSize** property setting on the number of records your application can handle at one time. For example, if you're using a **Recordset** object as the source of the data to be displayed on screen, you could set its **CacheSize** property to 20 to display 20 records at one time.</span></span>

<span data-ttu-id="e4716-121">Microsoft Access データベース エンジンでは、キャッシュ範囲内のレコードはキャッシュに要求し、キャッシュ範囲外のレコードはサーバーに対して要求します。</span><span class="sxs-lookup"><span data-stu-id="e4716-121">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="e4716-122">キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。</span><span class="sxs-lookup"><span data-stu-id="e4716-122">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data.</span></span>

<span data-ttu-id="e4716-123">キャッシュしたすべてのデータの更新を強制するには、 **Recordset** オブジェクトの **CacheSize** プロパティを 0 に設定し、次に、最初に要求したキャッシュのサイズにリセットしてから、 **FillCache** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e4716-123">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

## <a name="example"></a><span data-ttu-id="e4716-124">例</span><span class="sxs-lookup"><span data-stu-id="e4716-124">Example</span></span>

<span data-ttu-id="e4716-p106">次の使用例では、 **CreateTableDef** メソッドと **FillCache** メソッド、および **CacheSize**、 **CacheStart**、 **SourceTableName** の各プロパティを使用して、リンク テーブルのレコードを 2 回列挙します。次に、50 件のレコードをキャッシュして、すべてのレコードを 2 回列挙します。最後に、リンク テーブルを使用して、キャッシュされていない実行とキャッシュされた実行のパフォーマンス統計を表示します。</span><span class="sxs-lookup"><span data-stu-id="e4716-p106">This example uses the **CreateTableDef** and **FillCache** methods and the **CacheSize**, **CacheStart** and **SourceTableName** properties to enumerate the records in a linked table twice. Then it enumerates the records twice with a 50-record cache. The example then displays the performance statistics for the uncached and cached runs through the linked table.</span></span>

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
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
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
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
