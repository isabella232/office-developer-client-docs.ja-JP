---
title: MAPI ユーティリティの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5f0e5c97-5089-47cb-b604-2292b2ff945c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4612b6f345d59d988013671758c6d0579aaa127d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569534"
---
# <a name="using-the-mapi-utilities"></a><span data-ttu-id="e18b3-103">MAPI ユーティリティの使用</span><span class="sxs-lookup"><span data-stu-id="e18b3-103">Using the MAPI Utilities</span></span>

  
  
<span data-ttu-id="e18b3-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e18b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e18b3-105">MAPI ユーティリティでは、その他の機能をサポートするためにテーブルのデータとデータ オブジェクトのプロパティ、およびさまざまな機能の構成します。</span><span class="sxs-lookup"><span data-stu-id="e18b3-105">The MAPI utilities are made up of table data and property data objects and a variety of functions to support miscellaneous features.</span></span> <span data-ttu-id="e18b3-106">これらのユーティリティを必要していないサービス ・ プロバイダーとの接続を確立するために MAPI サブシステムにログオンするクライアントのことができます。</span><span class="sxs-lookup"><span data-stu-id="e18b3-106">It is possible for a client to need only these utilities and not have to log on to the MAPI subsystem to establish a connection with service providers.</span></span> <span data-ttu-id="e18b3-107">API 関数[ScInitMapiUtil](scinitmapiutil.md)を呼び出す場合は、クライアントは、このカテゴリに適合して、初期化時に[生じます](mapiinitialize.md)関数ではなく。</span><span class="sxs-lookup"><span data-stu-id="e18b3-107">If your client fits into this category, call the API function [ScInitMapiUtil](scinitmapiutil.md) rather than the [MAPIInitialize](mapiinitialize.md) function at initialization time.</span></span> 
  
 <span data-ttu-id="e18b3-108">**ScInitMapiUtil**は、MAPI のアロケーターを必要とするが、ことを要求しない、アロケーターに明示的に、ユーティリティ関数を使用するクライアントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="e18b3-108">**ScInitMapiUtil** enables clients to use utility functions that require MAPI allocators, but that do not ask for the allocators explicitly.</span></span> <span data-ttu-id="e18b3-109">シャット ダウンに時間がある場合は、 [MAPIUninitialize](mapiuninitialize.md)ではなく、リソースを解放するのには[DeinitMapiUtil](deinitmapiutil.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e18b3-109">When it is time to shut down, call [DeinitMapiUtil](deinitmapiutil.md) to free resources rather than [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="e18b3-110">**生じます**を呼び出すことはありませんクライアントは、 **MAPIUninitialize**を呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="e18b3-110">Clients that never call **MAPIInitialize** should not call **MAPIUninitialize**.</span></span>
  
<span data-ttu-id="e18b3-111">**生じます**ではなく、 **ScInitMapiUtil**を呼び出しています**IMAPITable**メソッドを使用せずに、 **ITableData**メソッドを使って、テーブルを使用するいるは、テーブルの通知は機能しないことに注意します。</span><span class="sxs-lookup"><span data-stu-id="e18b3-111">If you have called **ScInitMapiUtil** rather than **MAPIInitialize** and are using tables through the **ITableData** methods rather than through the **IMAPITable** methods, be aware that table notifications will not work.</span></span> <span data-ttu-id="e18b3-112">通知は、MAPI ライブラリの使用を必要として[IMAPITable: IUnknown](imapitableiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="e18b3-112">Notifications require the use of the MAPI libraries and [IMAPITable : IUnknown](imapitableiunknown.md).</span></span>
  

