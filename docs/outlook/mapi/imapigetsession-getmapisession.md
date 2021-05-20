---
title: IMAPIGetSessionGetMAPISession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIGetSession.GetMAPISession
api_type:
- COM
ms.assetid: 581db5d9-35f7-43ad-aef3-a5d5da310150
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dbf9f9f73d9e3860b482f81fb942673e6d373267
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439612"
---
# <a name="imapigetsessiongetmapisession"></a><span data-ttu-id="d5b0e-103">IMAPIGetSession::GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="d5b0e-103">IMAPIGetSession::GetMAPISession</span></span>

  
  
<span data-ttu-id="d5b0e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5b0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5b0e-105">MAPI サポート オブジェクトに関連付けられた MAPI セッションへのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="d5b0e-105">Returns a pointer to the MAPI session associated with the MAPI support object.</span></span>
  
```cpp
HRESULT GetMAPISession(
  LPUNKNOWN *  lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="d5b0e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d5b0e-106">Parameters</span></span>

 <span data-ttu-id="d5b0e-107">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="d5b0e-107">_lppSession_</span></span>
  
> <span data-ttu-id="d5b0e-108">[out]現在の MAPI セッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5b0e-108">[out] A pointer to the current MAPI session.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d5b0e-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5b0e-109">See also</span></span>



[<span data-ttu-id="d5b0e-110">IMAPIGetSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5b0e-110">IMAPIGetSession : IUnknown</span></span>](imapigetsessioniunknown.md)


[<span data-ttu-id="d5b0e-111">サポート オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="d5b0e-111">Support Object Overview</span></span>](support-object-overview.md)

