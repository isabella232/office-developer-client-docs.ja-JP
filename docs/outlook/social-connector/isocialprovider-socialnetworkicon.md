---
title: i////provideralnetworkicon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: ソーシャルネットワークのアイコンを表すバイト配列を返します。
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285499"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="b03aa-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="b03aa-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="b03aa-104">ソーシャルネットワークのアイコンを表すバイト配列を返します。</span><span class="sxs-lookup"><span data-stu-id="b03aa-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="b03aa-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="b03aa-105">Property value</span></span>

<span data-ttu-id="b03aa-106">ソーシャルネットワークのアイコンを含むバイトの配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b03aa-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b03aa-107">解説</span><span class="sxs-lookup"><span data-stu-id="b03aa-107">Remarks</span></span>

<span data-ttu-id="b03aa-108">サポートされている画像リソースは、.bmp、.jpeg、および .png 形式です。</span><span class="sxs-lookup"><span data-stu-id="b03aa-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b03aa-109">関連項目</span><span class="sxs-lookup"><span data-stu-id="b03aa-109">See also</span></span>

- [<span data-ttu-id="b03aa-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b03aa-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

