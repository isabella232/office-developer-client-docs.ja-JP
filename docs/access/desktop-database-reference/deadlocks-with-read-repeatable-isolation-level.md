---
title: 分離レベルが繰り返し可能な読み取りのときにデッドロックが発生する
TOCTitle: Deadlocks With Read Repeatable Isolation Level
ms:assetid: 3d5f3293-33bb-cf6d-362a-278f9ec1bd3c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249165(v=office.15)
ms:contentKeyID: 48544342
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de936da2772b809199d3890140683afd5ef01659
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476798"
---
# <a name="deadlocks-with-read-repeatable-isolation-level"></a><span data-ttu-id="b1e46-102">分離レベルが繰り返し可能な読み取りのときにデッドロックが発生する</span><span class="sxs-lookup"><span data-stu-id="b1e46-102">Deadlocks With Read Repeatable Isolation Level</span></span>


<span data-ttu-id="b1e46-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1e46-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b1e46-p101">カスタム ビジネス オブジェクトが繰り返し可能な読み取りの分離レベルを使用して SQL Server にアクセスする場合に、そのビジネス オブジェクトが、同じトランザクションでクエリを送信し更新する 2 つのクライアントによって同時に呼び出されると、デッドロックが発生する可能性があります。リモート データ サービスは、いずれか 1 つのプロセスをタイムアウトにしてデッドロックを解除できるように設計されていますが、そのクライアントの更新は失敗します。</span><span class="sxs-lookup"><span data-stu-id="b1e46-p101">If a custom business object uses an isolation level of read repeatable to access a SQL Server, and the business object is called simultaneously by two clients that send a query and update in the same transaction, a deadlock is possible. Remote Data Service is designed to allow one of the processes to time out to release the deadlock, but the update will fail for that client.</span></span>

<span data-ttu-id="b1e46-106">タイムアウトの長さを変更するのにには、[カーソル サービス](microsoft-cursor-service-for-ole-db-ado-service-component.md)**コマンドのタイムアウト**の動的プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="b1e46-106">Use the [Cursor Service](microsoft-cursor-service-for-ole-db-ado-service-component.md)**Command Time Out** dynamic property to modify the length of the timeout.</span></span>

