---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: 自動構成された ISocialSession インターフェイスを取得します。
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285780"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="52ef9-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="52ef9-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="52ef9-104">自動構成された [ISocialSession](isocialsessioniunknown.md) インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="52ef9-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="52ef9-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="52ef9-105">Parameters</span></span>

<span data-ttu-id="52ef9-106">_session_</span><span class="sxs-lookup"><span data-stu-id="52ef9-106">_session_</span></span>
  
> <span data-ttu-id="52ef9-107">[out] **ISocialSession** インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="52ef9-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="52ef9-108">注釈</span><span class="sxs-lookup"><span data-stu-id="52ef9-108">Remarks</span></span>

<span data-ttu-id="52ef9-109">返される **ISocialSession** インターフェイスは、プロバイダー固有のメソッドに基づき、自動的にネットワークにログオンされます。</span><span class="sxs-lookup"><span data-stu-id="52ef9-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="52ef9-110">ソーシャル ネットワークで自動構成をサポートしていない場合、プロバイダーは OSC_E_NOT_IMPLEMENTED エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="52ef9-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="52ef9-111">エラー コードの詳細については、「[Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52ef9-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="52ef9-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="52ef9-112">See also</span></span>

- [<span data-ttu-id="52ef9-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52ef9-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

