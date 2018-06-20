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
ms.openlocfilehash: b86a2d1c14c444ba79db495a3795dc61b1fe3660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804482"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="05f60-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="05f60-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="05f60-104">ソーシャル ネットワークのアイコンを表すバイトの配列を返します。</span><span class="sxs-lookup"><span data-stu-id="05f60-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="05f60-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="05f60-105">Property value</span></span>

<span data-ttu-id="05f60-106">ソーシャル ネットワークのアイコンが含まれているバイトの配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="05f60-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="05f60-107">備考</span><span class="sxs-lookup"><span data-stu-id="05f60-107">Remarks</span></span>

<span data-ttu-id="05f60-108">画像がサポートされているリソースとは、.bmp、.jpeg、および .png 形式です。</span><span class="sxs-lookup"><span data-stu-id="05f60-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="05f60-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="05f60-109">See also</span></span>

- [<span data-ttu-id="05f60-110">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="05f60-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

