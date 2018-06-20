---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: このソーシャル ネットワーク プロバイダーのバージョン番号を表す文字列を返します。
ms.openlocfilehash: 5c82df2dc4c052b1a06bcecb16defbb4dee38b18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804357"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="d65f5-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="d65f5-103">ISocialProvider::Version</span></span>

<span data-ttu-id="d65f5-104">このソーシャル ネットワーク プロバイダーのバージョン番号を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d65f5-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="d65f5-105">プロパティ値</span><span class="sxs-lookup"><span data-stu-id="d65f5-105">Property value</span></span>

<span data-ttu-id="d65f5-106">プロバイダーのバージョン番号を含む文字列です。</span><span class="sxs-lookup"><span data-stu-id="d65f5-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d65f5-107">備考</span><span class="sxs-lookup"><span data-stu-id="d65f5-107">Remarks</span></span>

<span data-ttu-id="d65f5-108">バージョン文字列は、 _MajorVersion_を使用してください。</span><span class="sxs-lookup"><span data-stu-id="d65f5-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="d65f5-109">_マイナー バージョン_の形式 (たとえば、1.4730) です。</span><span class="sxs-lookup"><span data-stu-id="d65f5-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d65f5-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="d65f5-110">See also</span></span>

- [<span data-ttu-id="d65f5-111">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d65f5-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

