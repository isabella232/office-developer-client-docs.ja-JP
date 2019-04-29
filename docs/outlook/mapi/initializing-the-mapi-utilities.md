---
title: MAPI ユーティリティの初期化
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02b14285-bbef-44f2-b2a4-45d96395998a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5c5a9355e9edec28e08986ccd055fc43eec7b974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420949"
---
# <a name="initializing-the-mapi-utilities"></a><span data-ttu-id="f72da-103">MAPI ユーティリティの初期化</span><span class="sxs-lookup"><span data-stu-id="f72da-103">Initializing the MAPI Utilities</span></span>

  
  
<span data-ttu-id="f72da-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f72da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f72da-105">使用する必要がある mapi の部分が、mapi の MAPIUTIL で宣言されているインターフェイスと関数である場合があります。H ヘッダーファイル ( **ipropdata**や**itabledata**など) — **MAPIInitialize**を呼び出して初期化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f72da-105">If the only part of MAPI that you need to use are the utilities — the interfaces and functions declared in MAPI's MAPIUTIL.H header file such as **IPropData** and **ITableData** — you do not need to call **MAPIInitialize** for initialization.</span></span> <span data-ttu-id="f72da-106">詳細については、「 [ipropdata: imapiprop](ipropdataimapiprop.md)」、「 [itabledata: IUnknown](itabledataiunknown.md)」、および「 [MAPIInitialize](mapiinitialize.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f72da-106">For more information, see [IPropData : IMAPIProp](ipropdataimapiprop.md), [ITableData : IUnknown](itabledataiunknown.md), and [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="f72da-107">代わりに、 **ScInitMapiUtil**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f72da-107">Instead, call the **ScInitMapiUtil** function.</span></span> <span data-ttu-id="f72da-108">詳細については、「 [ScInitMapiUtil](scinitmapiutil.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f72da-108">For more information, see [ScInitMapiUtil](scinitmapiutil.md).</span></span> <span data-ttu-id="f72da-109">**ScInitMapiUtil**では、クライアントアプリケーションが MAPI allocators を必要とするユーティリティ関数およびメソッドを使用できますが、それらを明示的には要求しません。</span><span class="sxs-lookup"><span data-stu-id="f72da-109">**ScInitMapiUtil** enables client applications to use utility functions and methods that require MAPI allocators, but that do not ask for them explicitly.</span></span> 
  
<span data-ttu-id="f72da-110">シャットダウン時に、 **DeinitMapiUtil**を呼び出して、ユーティリティに接続されているリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="f72da-110">At shutdown time, make a call to **DeinitMapiUtil** to free resources connected to the utilities.</span></span> <span data-ttu-id="f72da-111">**MAPIUninitialize**は呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="f72da-111">Do not call **MAPIUninitialize**.</span></span> <span data-ttu-id="f72da-112">詳細については、「 [DeinitMapiUtil](deinitmapiutil.md) 」と「 [MAPIUninitialize](mapiuninitialize.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f72da-112">For more information, see [DeinitMapiUtil](deinitmapiutil.md) and [MAPIUninitialize](mapiuninitialize.md).</span></span>
  
<span data-ttu-id="f72da-113">**itabledata**インターフェイスは、 **MAPIInitialize**ではなく**ScInitMapiUtil**を呼び出したクライアントのテーブル通知をサポートしていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f72da-113">Be aware that the **ITableData** interface does not support table notifications for clients that have called **ScInitMapiUtil** rather than **MAPIInitialize**.</span></span> 
  

