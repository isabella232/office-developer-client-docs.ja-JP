---
title: MAPI ユーティリティの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d8ec18ee7b80d8603266cf827f9484ee85bdb03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409987"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="b622e-103">MAPI ユーティリティの使用</span><span class="sxs-lookup"><span data-stu-id="b622e-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="b622e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b622e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b622e-105">MAPI ユーティリティは、テーブル データとプロパティ データ オブジェクトと、その他の機能をサポートするさまざまな機能でででています。</span><span class="sxs-lookup"><span data-stu-id="b622e-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="b622e-106">クライアントがこれらのユーティリティのみを必要とし、MAPI サブシステムにログオンしてサービス プロバイダーとの接続を確立する必要が生じ得る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b622e-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="b622e-107">クライアントがこのカテゴリに適合する場合は、初期化時に[MAPIInitialize](mapiinitialize.md)関数ではなく API 関数[ScInitMapiUtil](scinitmapiutil.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b622e-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="b622e-108">**ScInitMapiUtil を使用** すると、クライアントは MAPI アロケーターを必要とするユーティリティ関数を使用できますが、割り当て子を明示的に要求することはできません。</span><span class="sxs-lookup"><span data-stu-id="b622e-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="b622e-109">シャットダウンする時間が近い場合は [、DEinitMapiUtil](deinitmapiutil.md) を呼び出して [、MAPIUninitialize ではなくリソースを解放します](mapiuninitialize.md)。</span><span class="sxs-lookup"><span data-stu-id="b622e-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="b622e-110">**MAPIInitialize を呼び出さないクライアントは\*\*\*\*、MAPIUninitialize を呼び出す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="b622e-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="b622e-111">**MAPIInitialize** ではなく **ScInitMapiUtil** を呼び出し **、IMAPITable** メソッドではなく **ITableData** メソッドを使用してテーブルを使用している場合は、テーブル通知は機能しません。</span><span class="sxs-lookup"><span data-stu-id="b622e-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="b622e-112">通知には、MAPI ライブラリと [IMAPITable : IUnknown の使用が必要です](imapitableiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="b622e-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

