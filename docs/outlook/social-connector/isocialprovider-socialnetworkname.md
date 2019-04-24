---
title: i指定 alprovider/networkname
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: ソーシャルネットワーク名を表す文字列を返します。
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285492"
---
# <a name="isocialprovidersocialnetworkname"></a><span data-ttu-id="02129-103">ISocialProvider::SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="02129-103">ISocialProvider::SocialNetworkName</span></span>

<span data-ttu-id="02129-104">ソーシャルネットワーク名を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="02129-104">Returns a string that represents the social network name.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a><span data-ttu-id="02129-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="02129-105">Property value</span></span>

<span data-ttu-id="02129-106">ソーシャルネットワーク名を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="02129-106">A string that contains the social network name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="02129-107">解説</span><span class="sxs-lookup"><span data-stu-id="02129-107">Remarks</span></span>

<span data-ttu-id="02129-108">Outlook social Connector (.osc) プロバイダーは、ソーシャルネットワーク名をローカライズする必要があります。</span><span class="sxs-lookup"><span data-stu-id="02129-108">Outlook Social Connector (OSC) providers should localize the social network name.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="02129-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="02129-109">See also</span></span>

- [<span data-ttu-id="02129-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02129-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

