---
title: Recordset2.CacheStart プロパティ (DAO)
TOCTitle: CacheStart Property
ms:assetid: 2e9c2b0d-b382-e4d6-9406-ace0e538a7b7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192239(v=office.15)
ms:contentKeyID: 48543989
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c44d70323976ade2017d406b628d3347b414f6aa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478894"
---
# <a name="recordset2cachestart-property-dao"></a><span data-ttu-id="f7c94-102">Recordset2.CacheStart プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="f7c94-102">Recordset2.CacheStart Property (DAO)</span></span>


<span data-ttu-id="f7c94-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7c94-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7c94-104">ODBC データ ソースからローカルでキャッシュされるデータを含むダイナセット タイプの Recordset オブジェクトの最初のレコードのブックマークを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="f7c94-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c94-105">構文</span><span class="sxs-lookup"><span data-stu-id="f7c94-105">Syntax</span></span>

<span data-ttu-id="f7c94-106">*式*です。CacheStart</span><span class="sxs-lookup"><span data-stu-id="f7c94-106">*expression* .CacheStart</span></span>

<span data-ttu-id="f7c94-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f7c94-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c94-108">注釈</span><span class="sxs-lookup"><span data-stu-id="f7c94-108">Remarks</span></span>

<span data-ttu-id="f7c94-p101">**Recordset** オブジェクトを使用してリモート サーバーからデータを取得する場合、データをキャッシュすることでパフォーマンスが向上します。キャッシュは、サーバーから直前に取得されたデータを格納するローカル メモリ内の領域で、ユーザーがアプリケーションの実行中にそのデータを再び要求する場合に便利です。ユーザーがデータを要求すると、Microsoft Access データベース エンジンは、時間がかかるサーバーからのデータ取得ではなく、要求されたデータがキャッシュにあるかどうかをまず確認します。キャッシュに保存されるのは、ODBC データ ソースのデータのみです。</span><span class="sxs-lookup"><span data-stu-id="f7c94-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="f7c94-p102">リンク テーブルなど、Microsoft Access データベース エンジンに接続された ODBC データ ソースは、すべてローカル キャッシュを使用できます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、 **CacheSize** プロパティと **[CacheStart](recordset2-cachestart-property-dao.md)** プロパティを設定した後、 **[FillCache](recordset2-fillcache-method-dao.md)** メソッドを使用するか、または **Move** メソッドを使用してレコードを 1 つずつ移動します。</span><span class="sxs-lookup"><span data-stu-id="f7c94-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset2-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset2-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="f7c94-p103">**CacheStart** プロパティの設定値は、キャッシュされる **Recordset** オブジェクトの最初のレコードのブックマークです。任意のレコードのブックマークを使用して、 **CacheStart** プロパティを設定できます。キャッシュを開始するレコードをカレント レコードにして、 **CacheStart** プロパティを **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティと同じ値に設定します。</span><span class="sxs-lookup"><span data-stu-id="f7c94-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset2-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="f7c94-118">Microsoft Access データベース エンジンは、キャッシュ範囲内のレコードはキャッシュから要求し、キャッシュ範囲外のレコードはサーバーから要求します。</span><span class="sxs-lookup"><span data-stu-id="f7c94-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="f7c94-119">キャッシュから取得したレコードには、他のユーザーが並行してソース データに加えた変更は反映されていません。</span><span class="sxs-lookup"><span data-stu-id="f7c94-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="f7c94-120">キャッシュされたすべてのデータを強制的に更新するには、 **Recordset** オブジェクトの **CacheSize** プロパティを 0 に設定し、最初に要求したキャッシュのサイズに再設定した後、 **FillCache** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7c94-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>
