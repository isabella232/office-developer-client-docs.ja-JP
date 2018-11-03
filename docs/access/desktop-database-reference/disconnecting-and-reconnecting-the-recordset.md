---
title: 接続を切断して、レコード セットを再接続します。
TOCTitle: Disconnecting and reconnecting the Recordset
ms:assetid: d608d95d-9a4e-17a1-107a-b88b77f3774c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250077(v=office.15)
ms:contentKeyID: 48547975
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac1bc4c9c9d6d149faeb18d73f17539e63a4147e
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943942"
---
# <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="bc665-102">接続を切断して、レコード セットを再接続します。</span><span class="sxs-lookup"><span data-stu-id="bc665-102">Disconnecting and reconnecting the Recordset</span></span>


<span data-ttu-id="bc665-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bc665-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="disconnecting-and-reconnecting-the-recordset"></a><span data-ttu-id="bc665-104">レコードセットの切断および再接続</span><span class="sxs-lookup"><span data-stu-id="bc665-104">Disconnecting and Reconnecting the Recordset</span></span>

<span data-ttu-id="bc665-105">ADO の最も強力な機能の 1 つは、クライアント側の**Recordset**を開くと、データ ソース、データ ソースから\**レコード セット\*\*\*を切断*する機能です。</span><span class="sxs-lookup"><span data-stu-id="bc665-105">One of the most powerful features found in ADO is the capability to open a client-side **Recordset** from a data source and then *disconnect* the **Recordset** from the data source.</span></span> <span data-ttu-id="bc665-106">**レコード セット**を切断すると、データ ソースへの接続を終了できます、それを維持するために使用するサーバー上のリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="bc665-106">Once the **Recordset** has been disconnected, the connection to the data source can be closed, thereby releasing the resources on the server used to maintain it.</span></span> <span data-ttu-id="bc665-107">表示し切断されているときに、**レコード セット**内のデータを編集後、データ ソースに再接続し、更新をバッチ モードで送信を続行できます。</span><span class="sxs-lookup"><span data-stu-id="bc665-107">You can continue to view and edit the data in the **Recordset** while it is disconnected and later reconnect to the data source and send your updates in batch mode.</span></span>

<span data-ttu-id="bc665-p102">**Recordset** を切断するには、カーソル位置を **adUseClient** に設定して開いたうえで、**ActiveConnection** プロパティを *Nothing* に設定します (C++ を使用している場合は、**ActiveConnection** を NULL に設定して切断する必要があります)。</span><span class="sxs-lookup"><span data-stu-id="bc665-p102">To disconnect a **Recordset**, open it with a cursor location of **adUseClient**, and then set the **ActiveConnection** property equal to *Nothing*. (C++ users should set the **ActiveConnection** equal to NULL to disconnect.)</span></span>

<span data-ttu-id="bc665-110">切断された **Recordset** は、この章の後半で **Recordset** の保存について説明するときに使用します。この保存操作は、クライアント コンピューターがネットワークに接続されていないときに、アプリケーションが **Recordset** 内のデータを使用できるようにする必要がある場合に対処するためのものです。</span><span class="sxs-lookup"><span data-stu-id="bc665-110">We will use a disconnected **Recordset** later in this chapter when we discuss **Recordset** persistence to address a scenario in which we need to have the data in a **Recordset** available to an application while the client computer is not connected to a network.</span></span>

