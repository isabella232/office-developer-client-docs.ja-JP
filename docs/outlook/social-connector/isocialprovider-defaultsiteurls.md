---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Outlook ソーシャル コネクタ (OSC) プロバイダーのサイトの Url を指定する文字列の配列を返します。
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804342"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="a9664-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="a9664-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="a9664-104">Outlook ソーシャル コネクタ (OSC) プロバイダーのサイトの Url を指定する文字列の配列を返します。</span><span class="sxs-lookup"><span data-stu-id="a9664-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="a9664-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="a9664-105">Property value</span></span>

<span data-ttu-id="a9664-106">OSC プロバイダーのサイトの Url を表す文字列の配列を指定する構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9664-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9664-107">備考</span><span class="sxs-lookup"><span data-stu-id="a9664-107">Remarks</span></span>

<span data-ttu-id="a9664-108">プロバイダーは、複数のサイトの Url をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="a9664-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="a9664-109">OSC では、選択したサイトの URL のプロバイダーを通知するために[ISocialSession::SiteUrl](isocialsession-siteurl.md)プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9664-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="a9664-110">OSC では、既定のサイトの URL として、配列の最初の要素を使用します。</span><span class="sxs-lookup"><span data-stu-id="a9664-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="a9664-111">プロバイダーは、サイトの URL の配列に追加の要素を返すことができますが、OSC を使用しないようにします。</span><span class="sxs-lookup"><span data-stu-id="a9664-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9664-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9664-112">See also</span></span>

- [<span data-ttu-id="a9664-113">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9664-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

