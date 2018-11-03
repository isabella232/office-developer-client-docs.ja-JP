---
title: カーソル位置の重要性
TOCTitle: The Significance of Cursor Location
ms:assetid: 57cf91a0-2612-b1ca-1c03-9c1ccb396b2e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249296(v=office.15)
ms:contentKeyID: 48544978
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7054e25cd5768a8016ae7ea58f551be7dbb90cec
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944397"
---
# <a name="significance-of-cursor-location"></a><span data-ttu-id="c5612-102">カーソル位置の重要性</span><span class="sxs-lookup"><span data-stu-id="c5612-102">Significance of cursor location</span></span>

<span data-ttu-id="c5612-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c5612-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c5612-104">すべてのカーソルは、そのデータを保持するために、一時的なリソースを使用します。</span><span class="sxs-lookup"><span data-stu-id="c5612-104">Every cursor uses temporary resources to hold its data.</span></span> <span data-ttu-id="c5612-105">これらのリソースは、メモリ、ディスクのページング ファイル、一時ディスク ファイル、またはデータベースにも一時的な記憶域にあります。</span><span class="sxs-lookup"><span data-stu-id="c5612-105">These resources can be memory, a disk paging file, temporary disk files, or even temporary storage in the database.</span></span> <span data-ttu-id="c5612-106">これらのリソースがクライアント コンピューター上にある場合、カーソルは*クライアント側*カーソルと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c5612-106">The cursor is called a *client-side* cursor when these resources are located on the client computer.</span></span> <span data-ttu-id="c5612-107">これらのリソースがサーバー上にある場合、カーソルは、*サーバー側*カーソルと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="c5612-107">The cursor is called a *server-side* cursor when these resources are located on the server.</span></span>

## <a name="client-side-cursors"></a><span data-ttu-id="c5612-108">クライアント側カーソル</span><span class="sxs-lookup"><span data-stu-id="c5612-108">Client-Side Cursors</span></span>

<span data-ttu-id="c5612-p102">ADO では、 **adUseClient** **CursorLocationEnum** を使用してクライアント側カーソルを指定します。キーセット カーソル以外のクライアント側カーソルでは、サーバーが結果セット全体をネットワーク経由でクライアント コンピューターに送信します。クライアント コンピューターは、カーソルおよび結果セットに必要な一時リソースを用意し、これを管理します。クライアント側アプリケーションは、結果セット全体を参照して、必要な行を判断できます。</span><span class="sxs-lookup"><span data-stu-id="c5612-p102">In ADO, call for a client-side cursor by using the **adUseClient** **CursorLocationEnum**. With a non-keyset client-side cursor, the server sends the entire result set across the network to the client computer. The client computer provides and manages the temporary resources needed by the cursor and result set. The client-side application can browse through the entire result set to determine which rows it requires.</span></span>

<span data-ttu-id="c5612-p103">静的クライアント側カーソル、およびキーセット方式のクライアント側カーソルでは、カーソルに多くの行が含まれる場合に、ワークステーションに多大な負荷がかかる可能性があります。すべてのカーソル ライブラリには、数千の行を含むカーソルを作成する機能が備わっていますが、そのような大きな行セットをフェッチするよう設計されているアプリケーションは、パフォーマンスが低い場合があります。もちろん例外はあります。アプリケーションによっては、大容量のクライアント側カーソルが最も適しており、パフォーマンスもそれほど低下しないものがあります。</span><span class="sxs-lookup"><span data-stu-id="c5612-p103">Static and keyset-driven client-side cursors may place a significant load on your workstation if they include too many rows. While all of the cursor libraries are capable of building cursors with thousands of rows, applications designed to fetch such large rowsets may perform poorly. There are exceptions, of course. For some applications, a large client-side cursor might be perfectly appropriate and performance might not be an issue.</span></span>

<span data-ttu-id="c5612-p104">クライアント側カーソルの明確な利点の 1 つは、反応が速いことです。結果セットがクライアント コンピューターにダウンロードされた後は、非常に迅速に行を参照できます。また、クライアント側カーソルを使用すると、カーソルに必要なリソースがサーバーではなく各クライアントで個別に用意されるため、一般にアプリケーションの拡張性が高いと言えます。</span><span class="sxs-lookup"><span data-stu-id="c5612-p104">One obvious benefit of the client-side cursor is quick response. After the result set has been downloaded to the client computer, browsing through the rows is very fast. Your application is generally more scalable with client-side cursors because the cursor's resource requirements are placed on each separate client and not on the server.</span></span>

## <a name="server-side-cursors"></a><span data-ttu-id="c5612-120">サーバー側カーソル</span><span class="sxs-lookup"><span data-stu-id="c5612-120">Server-Side Cursors</span></span>

<span data-ttu-id="c5612-p105">ADO では、 **adUseServer** **CursorLocationEnum** を使用してサーバー側カーソルを指定します。サーバー側カーソルを使用する場合、サーバー コンピューターに用意されたリソースを使用して、サーバーが結果セットを管理します。サーバー側カーソルは、要求されたデータのみをネットワーク経由で返します。この種類のカーソルを使用すると、特にネットワーク トラフィックの混雑が問題となる状況では、クライアント側カーソルよりも高いパフォーマンスを得ることができる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c5612-p105">In ADO, call for a server-side cursor by using the **adUseServer** **CursorLocationEnum.** With a server-side cursor, the server manages the result set using resources provided by the server computer. The server-side cursor returns only the requested data over the network. This type of cursor can sometimes provide better performance than the client-side cursor, especially in situations where excessive network traffic is a problem.</span></span>

<span data-ttu-id="c5612-p106">しかし、サーバー側カーソルは、少なくとも一時的には、すべてのアクティブなクライアントについて、貴重なサーバーのリソースを消費してしまうため、注意する必要があります。このことを考慮して、アクティブなクライアントから要求されるすべてのサーバー側カーソルを管理できるだけのサーバー ハードウェアを用意するよう計画する必要があります。また、サーバー側カーソルでは、単一の行にしかアクセスできない (バッチ カーソルが利用できない) ため、処理に時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c5612-p106">However, it is important to point out that a server-side cursor is — at least temporarily — consuming precious server resources for every active client. You must plan accordingly to ensure that your server hardware is capable of managing all of the server-side cursors requested by active clients. Also, a server-side cursor can be slow because it provides only single row access — there is no batch cursor available.</span></span>

<span data-ttu-id="c5612-p107">サーバー側カーソルは、レコードを挿入、更新、または削除するときに便利です。サーバー側カーソルを使用すると、同じ接続に複数のアクティブなステートメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c5612-p107">Server-side cursors are useful when inserting, updating, or deleting records. With server-side cursors, you can have multiple active statements on the same connection.</span></span>

