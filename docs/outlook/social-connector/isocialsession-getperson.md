---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: userID パラメーターに基づいて ISocialPerson インターフェイスを取得します。
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439822"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="c1b1e-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="c1b1e-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="c1b1e-104">userID [パラメーターに基づいて ISocialPerson](isocialpersoniunknown.md) インターフェイス  _を取得_ します。</span><span class="sxs-lookup"><span data-stu-id="c1b1e-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="c1b1e-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c1b1e-105">Parameters</span></span>

<span data-ttu-id="c1b1e-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="c1b1e-106">_userId_</span></span>
  
> <span data-ttu-id="c1b1e-107">[in]ユーザーのユーザー ID または SMTP アドレスを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="c1b1e-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="c1b1e-108">_result_</span><span class="sxs-lookup"><span data-stu-id="c1b1e-108">_result_</span></span>
  
> <span data-ttu-id="c1b1e-109">[out] **ISocialPerson** インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="c1b1e-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c1b1e-110">注釈</span><span class="sxs-lookup"><span data-stu-id="c1b1e-110">Remarks</span></span>

<span data-ttu-id="c1b1e-111">_userID パラメーターは_、ユーザー ID または SMTP アドレスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1b1e-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c1b1e-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1b1e-112">See also</span></span>

- [<span data-ttu-id="c1b1e-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1b1e-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

