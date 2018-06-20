---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: ソーシャル ネットワークの一意の識別子を表す GUID を返します。
ms.openlocfilehash: 5ff10d51fab03c3bca3eead52848088f2cd80bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804371"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="e59d8-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="e59d8-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="e59d8-104">ソーシャル ネットワークの一意の識別子を表す GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="e59d8-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="e59d8-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="e59d8-105">Property value</span></span>

<span data-ttu-id="e59d8-106">ソーシャル ネットワークの一意の識別子を表す GUID 値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e59d8-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e59d8-107">備考</span><span class="sxs-lookup"><span data-stu-id="e59d8-107">Remarks</span></span>

<span data-ttu-id="e59d8-108">GUID は不変である必要があり、プロバイダーのバージョンが変更された場合でも変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e59d8-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e59d8-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="e59d8-109">See also</span></span>

- [<span data-ttu-id="e59d8-110">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e59d8-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

