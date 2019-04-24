---
title: 読み取り反復可能分離レベルを持つデッドロック
TOCTitle: Deadlocks with read repeatable isolation level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c3e38f6054e6548dfc14d30ce6ec89dcb2e4b01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294177"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="c9a5c-102">読み取り反復可能分離レベルを持つデッドロック</span><span class="sxs-lookup"><span data-stu-id="c9a5c-102">Deadlocks with read repeatable isolation level</span></span>


<span data-ttu-id="c9a5c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9a5c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9a5c-p101">カスタム ビジネス オブジェクトが繰り返し可能な読み取りの分離レベルを使用して SQL Server にアクセスする場合に、そのビジネス オブジェクトが、同じトランザクションでクエリを送信し更新する 2 つのクライアントによって同時に呼び出されると、デッドロックが発生する可能性があります。リモート データ サービスは、いずれか 1 つのプロセスをタイムアウトにしてデッドロックを解除できるように設計されていますが、そのクライアントの更新は失敗します。</span><span class="sxs-lookup"><span data-stu-id="c9a5c-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="c9a5c-106">タイムアウトの長さを変更するには、 [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**コマンド**のタイムアウトの動的プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c9a5c-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

