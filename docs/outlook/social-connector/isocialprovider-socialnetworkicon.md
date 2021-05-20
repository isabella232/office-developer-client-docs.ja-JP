---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: ソーシャル ネットワークのアイコンを表すバイトの配列を返します。
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438688"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="c40e5-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="c40e5-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="c40e5-104">ソーシャル ネットワークのアイコンを表すバイトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="c40e5-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="c40e5-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="c40e5-105">Property value</span></span>

<span data-ttu-id="c40e5-106">ソーシャル ネットワークのアイコンを含むバイトの配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c40e5-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c40e5-107">注釈</span><span class="sxs-lookup"><span data-stu-id="c40e5-107">Remarks</span></span>

<span data-ttu-id="c40e5-108">サポートされているピクチャ リソースは、.bmp.jpeg、および .png形式です。</span><span class="sxs-lookup"><span data-stu-id="c40e5-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c40e5-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="c40e5-109">See also</span></span>

- [<span data-ttu-id="c40e5-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c40e5-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

