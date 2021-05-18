---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: ソーシャル ネットワーク名を表す文字列を返します。
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406879"
---
# <a name="isocialprovidersocialnetworkname"></a><span data-ttu-id="b43d4-103">ISocialProvider::SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="b43d4-103">ISocialProvider::SocialNetworkName</span></span>

<span data-ttu-id="b43d4-104">ソーシャル ネットワーク名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="b43d4-104">Returns a string that represents the social network name.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a><span data-ttu-id="b43d4-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="b43d4-105">Property value</span></span>

<span data-ttu-id="b43d4-106">ソーシャル ネットワーク名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="b43d4-106">A string that contains the social network name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b43d4-107">注釈</span><span class="sxs-lookup"><span data-stu-id="b43d4-107">Remarks</span></span>

<span data-ttu-id="b43d4-108">Outlookソーシャル コネクタ (OSC) プロバイダーは、ソーシャル ネットワーク名をローカライズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b43d4-108">Outlook Social Connector (OSC) providers should localize the social network name.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b43d4-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="b43d4-109">See also</span></span>

- [<span data-ttu-id="b43d4-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b43d4-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

