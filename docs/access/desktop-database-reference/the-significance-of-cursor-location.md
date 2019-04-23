---
title: カーソル位置の重要性
TOCTitle: The Significance of Cursor Location
ms:assetid: 57cf91a0-2612-b1ca-1c03-9c1ccb396b2e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249296(v=office.15)
ms:contentKeyID: 48544978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3ae9cc65d61416767140572b32d3f2e1b8e4d8eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313980"
---
# <a name="significance-of-cursor-location"></a><span data-ttu-id="318f2-102">カーソル位置の重要性</span><span class="sxs-lookup"><span data-stu-id="318f2-102">Significance of cursor location</span></span>

<span data-ttu-id="318f2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="318f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="318f2-p101">すべてのカーソルは、一時リソースを使用してデータを保持します。これらのリソースには、メモリ、ディスク上のページング ファイル、ディスク上の一時ファイルの他、データベース内の一時記憶域が使用される場合もあります。これらのリソースがクライアント コンピューター側にある場合、そのカーソルは "クライアント側" カーソルと呼ばれます。一方、これらのリソースがサーバー上にある場合、そのカーソルは "サーバー側" カーソルと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="318f2-p101">Every cursor uses temporary resources to hold its data. These resources can be memory, a disk paging file, temporary disk files, or even temporary storage in the database. The cursor is called a *client-side* cursor when these resources are located on the client computer. The cursor is called a *server-side* cursor when these resources are located on the server.</span></span>

## <a name="client-side-cursors"></a><span data-ttu-id="318f2-108">クライアント側カーソル</span><span class="sxs-lookup"><span data-stu-id="318f2-108">Client-Side Cursors</span></span>

<span data-ttu-id="318f2-p102">ADO では、 **adUseClient** **CursorLocationEnum** を使用してクライアント側カーソルを指定します。キーセット カーソル以外のクライアント側カーソルでは、サーバーが結果セット全体をネットワーク経由でクライアント コンピューターに送信します。クライアント コンピューターは、カーソルおよび結果セットに必要な一時リソースを用意し、これを管理します。クライアント側アプリケーションは、結果セット全体を参照して、必要な行を判断できます。</span><span class="sxs-lookup"><span data-stu-id="318f2-p102">In ADO, call for a client-side cursor by using the **adUseClient** **CursorLocationEnum**. With a non-keyset client-side cursor, the server sends the entire result set across the network to the client computer. The client computer provides and manages the temporary resources needed by the cursor and result set. The client-side application can browse through the entire result set to determine which rows it requires.</span></span>

<span data-ttu-id="318f2-p103">静的クライアント側カーソル、およびキーセット方式のクライアント側カーソルでは、カーソルに多くの行が含まれる場合に、ワークステーションに多大な負荷がかかる可能性があります。すべてのカーソル ライブラリには、数千の行を含むカーソルを作成する機能が備わっていますが、そのような大きな行セットをフェッチするよう設計されているアプリケーションは、パフォーマンスが低い場合があります。もちろん例外はあります。アプリケーションによっては、大容量のクライアント側カーソルが最も適しており、パフォーマンスもそれほど低下しないものがあります。</span><span class="sxs-lookup"><span data-stu-id="318f2-p103">Static and keyset-driven client-side cursors may place a significant load on your workstation if they include too many rows. While all of the cursor libraries are capable of building cursors with thousands of rows, applications designed to fetch such large rowsets may perform poorly. There are exceptions, of course. For some applications, a large client-side cursor might be perfectly appropriate and performance might not be an issue.</span></span>

<span data-ttu-id="318f2-p104">クライアント側カーソルの明確な利点の 1 つは、反応が速いことです。結果セットがクライアント コンピューターにダウンロードされた後は、非常に迅速に行を参照できます。また、クライアント側カーソルを使用すると、カーソルに必要なリソースがサーバーではなく各クライアントで個別に用意されるため、一般にアプリケーションの拡張性が高いと言えます。</span><span class="sxs-lookup"><span data-stu-id="318f2-p104">One obvious benefit of the client-side cursor is quick response. After the result set has been downloaded to the client computer, browsing through the rows is very fast. Your application is generally more scalable with client-side cursors because the cursor's resource requirements are placed on each separate client and not on the server.</span></span>

## <a name="server-side-cursors"></a><span data-ttu-id="318f2-120">サーバー側カーソル</span><span class="sxs-lookup"><span data-stu-id="318f2-120">Server-Side Cursors</span></span>

<span data-ttu-id="318f2-p105">ADO では、 **adUseServer** **CursorLocationEnum** を使用してサーバー側カーソルを指定します。サーバー側カーソルを使用する場合、サーバー コンピューターに用意されたリソースを使用して、サーバーが結果セットを管理します。サーバー側カーソルは、要求されたデータのみをネットワーク経由で返します。この種類のカーソルを使用すると、特にネットワーク トラフィックの混雑が問題となる状況では、クライアント側カーソルよりも高いパフォーマンスを得ることができる場合があります。</span><span class="sxs-lookup"><span data-stu-id="318f2-p105">In ADO, call for a server-side cursor by using the **adUseServer** **CursorLocationEnum.** With a server-side cursor, the server manages the result set using resources provided by the server computer. The server-side cursor returns only the requested data over the network. This type of cursor can sometimes provide better performance than the client-side cursor, especially in situations where excessive network traffic is a problem.</span></span>

<span data-ttu-id="318f2-p106">しかし、サーバー側カーソルは、少なくとも一時的には、すべてのアクティブなクライアントについて、貴重なサーバーのリソースを消費してしまうため、注意する必要があります。このことを考慮して、アクティブなクライアントから要求されるすべてのサーバー側カーソルを管理できるだけのサーバー ハードウェアを用意するよう計画する必要があります。また、サーバー側カーソルでは、単一の行にしかアクセスできない (バッチ カーソルが利用できない) ため、処理に時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="318f2-p106">However, it is important to point out that a server-side cursor is — at least temporarily — consuming precious server resources for every active client. You must plan accordingly to ensure that your server hardware is capable of managing all of the server-side cursors requested by active clients. Also, a server-side cursor can be slow because it provides only single row access — there is no batch cursor available.</span></span>

<span data-ttu-id="318f2-p107">サーバー側カーソルは、レコードを挿入、更新、または削除するときに便利です。サーバー側カーソルを使用すると、同じ接続に複数のアクティブなステートメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="318f2-p107">Server-side cursors are useful when inserting, updating, or deleting records. With server-side cursors, you can have multiple active statements on the same connection.</span></span>

