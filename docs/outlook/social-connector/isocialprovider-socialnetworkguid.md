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
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407873"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="09b49-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="09b49-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="09b49-104">ソーシャル ネットワークの一意の識別子を表す GUID を返します。</span><span class="sxs-lookup"><span data-stu-id="09b49-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="09b49-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="09b49-105">Property value</span></span>

<span data-ttu-id="09b49-106">ソーシャル ネットワークの一意の識別子を表す GUID 値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="09b49-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09b49-107">注釈</span><span class="sxs-lookup"><span data-stu-id="09b49-107">Remarks</span></span>

<span data-ttu-id="09b49-108">GUID は変更できない必要があります。プロバイダーのバージョンが変更された場合でも変更できません。</span><span class="sxs-lookup"><span data-stu-id="09b49-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="09b49-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="09b49-109">See also</span></span>

- [<span data-ttu-id="09b49-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09b49-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

