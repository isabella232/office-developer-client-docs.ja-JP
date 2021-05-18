---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: ソーシャル コネクタOutlook (OSC) プロバイダーを初期化します。
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285760"
---
# <a name="isocialproviderload"></a><span data-ttu-id="028e8-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="028e8-103">ISocialProvider::Load</span></span>

<span data-ttu-id="028e8-104">ソーシャル コネクタOutlook (OSC) プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="028e8-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="028e8-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="028e8-105">Parameters</span></span>

<span data-ttu-id="028e8-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="028e8-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="028e8-107">[in]OSC で予期される OSC プロバイダー インターフェイスのバージョン。</span><span class="sxs-lookup"><span data-stu-id="028e8-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="028e8-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="028e8-108">_languageTag_</span></span>
  
> <span data-ttu-id="028e8-109">[in][[RFC4646] および [RFC4647]](https://www.ietf.org/rfc/rfc4646.txt)で定義されるインターネット[](https://www.ietf.org/rfc/rfc4647.txt)エンジニアリング タスク フォース (IETF) 言語タグは、現在の Outlook ユーザー インターフェイス言語を表します。</span><span class="sxs-lookup"><span data-stu-id="028e8-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="028e8-110">注釈</span><span class="sxs-lookup"><span data-stu-id="028e8-110">Remarks</span></span>

<span data-ttu-id="028e8-111">_socialProviderInterfaceVersion_ パラメーターのバージョン形式は _X です_。_xxxx_ _、X_ はメジャー バージョン _、xxxx_ は OSC のマイナー バージョンです。</span><span class="sxs-lookup"><span data-stu-id="028e8-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="028e8-112">2013 Office、メジャー バージョンが 15 か確認してください。</span><span class="sxs-lookup"><span data-stu-id="028e8-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="028e8-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="028e8-113">See also</span></span>

- [<span data-ttu-id="028e8-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="028e8-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

