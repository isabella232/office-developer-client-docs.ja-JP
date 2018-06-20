---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: 自動的に構成されている ISocialSession インターフェイスを取得します。
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804374"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="94bc2-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="94bc2-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="94bc2-104">自動的に構成されている[ISocialSession](isocialsessioniunknown.md)インターフェイスを取得します。</span><span class="sxs-lookup"><span data-stu-id="94bc2-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="94bc2-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="94bc2-105">Parameters</span></span>

<span data-ttu-id="94bc2-106">_セッション_</span><span class="sxs-lookup"><span data-stu-id="94bc2-106">_session_</span></span>
  
> <span data-ttu-id="94bc2-107">[out]**ISocialSession**インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="94bc2-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="94bc2-108">備考</span><span class="sxs-lookup"><span data-stu-id="94bc2-108">Remarks</span></span>

<span data-ttu-id="94bc2-109">返される**ISocialSession**インターフェイスは、プロバイダーに固有のメソッドに基づき、ネットワークに自動的にログオンします。</span><span class="sxs-lookup"><span data-stu-id="94bc2-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="94bc2-110">プロバイダーは、ソーシャル ネットワークでは、自動構成をサポートしていない場合、OSC_E_NOT_IMPLEMENTED エラーを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="94bc2-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="94bc2-111">エラー コードの詳細については、 [Outlook ソーシャル コネクタ プロバイダーのエラー コード](outlook-social-connector-provider-error-codes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="94bc2-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="94bc2-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="94bc2-112">See also</span></span>

- [<span data-ttu-id="94bc2-113">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="94bc2-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

