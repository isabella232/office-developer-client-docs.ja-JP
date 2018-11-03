---
title: ロック (デスクトップ データベース参照のアクセス) の種類
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a104b2ad452cdf8b0688dbc84ca09b90ed08c62
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944915"
---
# <a name="types-of-locks"></a><span data-ttu-id="b20fe-102">ロックの種類</span><span class="sxs-lookup"><span data-stu-id="b20fe-102">Types of locks</span></span>


<span data-ttu-id="b20fe-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b20fe-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="adlockbatchoptimistic"></a><span data-ttu-id="b20fe-104">adLockBatchOptimistic</span><span class="sxs-lookup"><span data-stu-id="b20fe-104">adLockBatchOptimistic</span></span>

<span data-ttu-id="b20fe-p101">共有的バッチ更新を示します。バッチ更新モードの場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="b20fe-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span>

<span data-ttu-id="b20fe-p102">多くのアプリケーションでは、一度に多数の行をフェッチした後、挿入、更新、または削除される行セット全体に対して調整したうえでの更新を行う必要があります。バッチ カーソルを使用すると、サーバーへの往復が 1 回で済むため、更新パフォーマンスが向上し、ネットワーク トラフィックが軽減されます。バッチ カーソル ライブラリを使用すると、静的カーソルを作成した後、データ ソースから切断できます。この時点で、行を変更した後、再接続し、変更内容をデータ ソースにまとめて送信することができます。</span><span class="sxs-lookup"><span data-stu-id="b20fe-p102">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted. With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic. Using a batch cursor library, you can create a static cursor and then disconnect from the data source. At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</span></span>

## <a name="adlockoptimistic"></a><span data-ttu-id="b20fe-111">adLockOptimistic</span><span class="sxs-lookup"><span data-stu-id="b20fe-111">adLockOptimistic</span></span>

<span data-ttu-id="b20fe-p103">**Update** メソッドを呼び出したときのみレコードをロックする、共有的ロックの使用を指定します。これは、レコードを編集してから **Update** を呼び出すまでに、他のユーザーがデータを変更し、競合が発生する可能性があることを示します。この種類のロックは、競合が発生する可能性が低いか、競合をすぐに解決できる状況で使用します。</span><span class="sxs-lookup"><span data-stu-id="b20fe-p103">Indicates that the provider uses optimistic locking — locking records only when you call the **Update** method. This means that there is a chance that the data may be changed by another user between the time you edit the record and when you call **Update**, which creates conflicts. Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</span></span>

## <a name="adlockpessimistic"></a><span data-ttu-id="b20fe-115">adLockPessimistic</span><span class="sxs-lookup"><span data-stu-id="b20fe-115">adLockPessimistic</span></span>

<span data-ttu-id="b20fe-p104">レコード単位の排他的ロックを指定します。プロバイダーは、レコードの編集が正常に行われることを確実にするために必要な操作 (通常は編集の直前にレコードに対するデータ ソースでのロック) を実行します。これは、編集を開始すると、 **Update** を呼び出してロックを解除するまで、他のユーザーがそのレコードを使用できないことを意味します。この種類のロックは、予約システムなど、データを同時に変更できないシステムで使用します。</span><span class="sxs-lookup"><span data-stu-id="b20fe-p104">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing. Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling **Update.** Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</span></span>

## <a name="adlockreadonly"></a><span data-ttu-id="b20fe-120">adLockReadOnly</span><span class="sxs-lookup"><span data-stu-id="b20fe-120">adLockReadOnly</span></span>

<span data-ttu-id="b20fe-p105">読み取り専用のレコードを指定します。データの変更はできません。読み取り専用ロックは、サーバーでレコードのロックを保持する必要がないため、"最も高速な" ロックです。</span><span class="sxs-lookup"><span data-stu-id="b20fe-p105">Indicates read-only records. You cannot alter the data. A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</span></span>

## <a name="adlockunspecified"></a><span data-ttu-id="b20fe-124">adLockUnspecified</span><span class="sxs-lookup"><span data-stu-id="b20fe-124">adLockUnspecified</span></span>

<span data-ttu-id="b20fe-125">ロックの種類を指定しません。</span><span class="sxs-lookup"><span data-stu-id="b20fe-125">Does not specify a type of lock.</span></span>

