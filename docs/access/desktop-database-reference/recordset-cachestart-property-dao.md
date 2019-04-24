---
title: Recordset. cachestart プロパティ (DAO)
TOCTitle: CacheStart Property
ms:assetid: 03814312-660a-d8e9-8a7b-bc14d66e05ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844802(v=office.15)
ms:contentKeyID: 48542986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053171
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 514f109f0eed902287e519bcd7a729397e70eaa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300617"
---
# <a name="recordsetcachestart-property-dao"></a><span data-ttu-id="d643d-102">Recordset. cachestart プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d643d-102">Recordset.CacheStart property (DAO)</span></span>


<span data-ttu-id="d643d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d643d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d643d-104">ODBC データ ソースからローカルでキャッシュされるデータを含むダイナセット タイプの Recordset オブジェクトの最初のレコードのブックマークを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="d643d-104">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d643d-105">構文</span><span class="sxs-lookup"><span data-stu-id="d643d-105">Syntax</span></span>

<span data-ttu-id="d643d-106">*式*。CacheStart</span><span class="sxs-lookup"><span data-stu-id="d643d-106">*expression* .CacheStart</span></span>

<span data-ttu-id="d643d-107">\*式\***Recordset**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d643d-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d643d-108">注釈</span><span class="sxs-lookup"><span data-stu-id="d643d-108">Remarks</span></span>

<span data-ttu-id="d643d-p101">**Recordset** オブジェクトを使用してリモート サーバーからデータを取得する場合、データをキャッシュすることでパフォーマンスが向上します。キャッシュは、サーバーから直前に取得されたデータを格納するローカル メモリ内の領域で、ユーザーがアプリケーションの実行中にそのデータを再び要求する場合に便利です。ユーザーがデータを要求すると、Microsoft Access データベース エンジンは、時間がかかるサーバーからのデータ取得ではなく、要求されたデータがキャッシュにあるかどうかをまず確認します。キャッシュに保存されるのは、ODBC データ ソースのデータのみです。</span><span class="sxs-lookup"><span data-stu-id="d643d-p101">Data caching improves performance if you use **Recordset** objects to retrieve data from a remote server. A cache is a space in local memory that holds the data most recently retrieved from the server; this is useful if users request the data again while the application is running. When users request data, the Microsoft Access database engine checks the cache for the requested data first rather than retrieving it from the server, which takes more time. The cache only saves data that comes from an ODBC data source.</span></span>

<span data-ttu-id="d643d-p102">リンク テーブルなど、Microsoft Access データベース エンジンに接続された ODBC データ ソースは、すべてローカル キャッシュを使用できます。キャッシュを作成するには、リモート データ ソースから **Recordset** オブジェクトを開き、 **CacheSize** プロパティと **[CacheStart](recordset-cachestart-property-dao.md)** プロパティを設定した後、 **[FillCache](recordset-fillcache-method-dao.md)** メソッドを使用するか、または **Move** メソッドを使用してレコードを 1 つずつ移動します。</span><span class="sxs-lookup"><span data-stu-id="d643d-p102">Any Microsoft Access database engine-connected ODBC data source, such as a linked table, can have a local cache. To create the cache, open a **Recordset** object from the remote data source, set the **CacheSize** and **[CacheStart](recordset-cachestart-property-dao.md)** properties, and then use the **[FillCache](recordset-fillcache-method-dao.md)** method, or step through the records by using the **Move** methods.</span></span>

<span data-ttu-id="d643d-p103">**CacheStart** プロパティの設定値は、キャッシュされる **Recordset** オブジェクトの最初のレコードのブックマークです。任意のレコードのブックマークを使用して、 **CacheStart** プロパティを設定できます。キャッシュを開始するレコードをカレント レコードにして、 **CacheStart** プロパティを **[Bookmark](recordset-bookmark-property-dao.md)** プロパティと同じ値に設定します。</span><span class="sxs-lookup"><span data-stu-id="d643d-p103">The **CacheStart** property setting is the bookmark of the first record in the **Recordset** object to be cached. You can use the bookmark of any record to set the **CacheStart** property. Make the record you want to start the cache the current record, and set the **CacheStart** property equal to the **[Bookmark](recordset-bookmark-property-dao.md)** property.</span></span>

<span data-ttu-id="d643d-118">Microsoft Access データベース エンジンは、キャッシュ範囲内のレコードはキャッシュから要求し、キャッシュ範囲外のレコードはサーバーから要求します。</span><span class="sxs-lookup"><span data-stu-id="d643d-118">The Microsoft Access database engine requests records within the cache range from the cache, and it requests records outside the cache range from the server.</span></span>

<span data-ttu-id="d643d-119">キャッシュから取得したレコードには、他のユーザーが並行してソース データに加えた変更は反映されていません。</span><span class="sxs-lookup"><span data-stu-id="d643d-119">Records retrieved from the cache don't reflect changes made concurrently to the source data by other users.</span></span>

<span data-ttu-id="d643d-120">キャッシュされたすべてのデータを強制的に更新するには、 **Recordset** オブジェクトの **CacheSize** プロパティを 0 に設定し、最初に要求したキャッシュのサイズに再設定した後、 **FillCache** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d643d-120">To force an update of all the cached data, set the **CacheSize** property of the **Recordset** object to 0, re-set it to the size of the cache you originally requested, and then use the **FillCache** method.</span></span>

