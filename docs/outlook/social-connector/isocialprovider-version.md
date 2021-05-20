---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を返します。
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438275"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="66552-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="66552-103">ISocialProvider::Version</span></span>

<span data-ttu-id="66552-104">このソーシャル ネットワークのプロバイダーのバージョン番号を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="66552-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="66552-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="66552-105">Property value</span></span>

<span data-ttu-id="66552-106">プロバイダーのバージョン番号を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="66552-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66552-107">注釈</span><span class="sxs-lookup"><span data-stu-id="66552-107">Remarks</span></span>

<span data-ttu-id="66552-108">バージョン文字列は  _MajorVersion を使用する必要があります_。</span><span class="sxs-lookup"><span data-stu-id="66552-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="66552-109">_MinorVersion_ 形式 (1.4730 など)。</span><span class="sxs-lookup"><span data-stu-id="66552-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="66552-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="66552-110">See also</span></span>

- [<span data-ttu-id="66552-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="66552-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

