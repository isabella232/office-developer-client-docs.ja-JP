---
title: i、alprovidergetsession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: i式 alsession インターフェイスを取得します。
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285773"
---
# <a name="isocialprovidergetsession"></a><span data-ttu-id="2d609-103">ISocialProvider::GetSession</span><span class="sxs-lookup"><span data-stu-id="2d609-103">ISocialProvider::GetSession</span></span>

<span data-ttu-id="2d609-104">i式[alsession](isocialsessioniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="2d609-104">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="2d609-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2d609-105">Parameters</span></span>

<span data-ttu-id="2d609-106">_session_</span><span class="sxs-lookup"><span data-stu-id="2d609-106">_session_</span></span>
  
> <span data-ttu-id="2d609-107">[out] **ISocialSession** インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="2d609-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2d609-108">注釈</span><span class="sxs-lookup"><span data-stu-id="2d609-108">Remarks</span></span>

<span data-ttu-id="2d609-109">Outlook social Connector (.osc) は、 **isocial alsession**インターフェイスを使用してソーシャルネットワークにログオンします。</span><span class="sxs-lookup"><span data-stu-id="2d609-109">The Outlook Social Connector (OSC) uses the **ISocialSession** interface to log on to the social network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d609-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d609-110">See also</span></span>

- [<span data-ttu-id="2d609-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d609-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

