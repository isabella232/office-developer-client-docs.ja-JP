---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: ソーシャル コネクタ (OSC) プロバイダーのサイト URL を指定Outlook文字列の配列を返します。
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413774"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="b72b9-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="b72b9-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="b72b9-104">ソーシャル コネクタ (OSC) プロバイダーのサイト URL を指定Outlook文字列の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="b72b9-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="b72b9-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="b72b9-105">Property value</span></span>

<span data-ttu-id="b72b9-106">OSC プロバイダーのサイト URL を表す文字列の配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b72b9-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b72b9-107">注釈</span><span class="sxs-lookup"><span data-stu-id="b72b9-107">Remarks</span></span>

<span data-ttu-id="b72b9-108">プロバイダーは、複数のサイト URL をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="b72b9-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="b72b9-109">OSC は [、ISocialSession::SiteUrl](isocialsession-siteurl.md) プロパティを設定して、選択したサイト URL をプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="b72b9-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="b72b9-110">OSC は、配列の最初の要素を既定のサイト URL として使用します。</span><span class="sxs-lookup"><span data-stu-id="b72b9-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="b72b9-111">プロバイダーは、サイト URL 配列内の追加の要素を返できますが、OSC はそれらを使用しません。</span><span class="sxs-lookup"><span data-stu-id="b72b9-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b72b9-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="b72b9-112">See also</span></span>

- [<span data-ttu-id="b72b9-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b72b9-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

