---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Outlook ソーシャル コネクタ (OSC) プロバイダーを初期化します。
ms.openlocfilehash: 172595db8d9467f22a80c8caf0e3444250826aaf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804354"
---
# <a name="isocialproviderload"></a><span data-ttu-id="d65a8-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="d65a8-103">ISocialProvider::Load</span></span>

<span data-ttu-id="d65a8-104">Outlook ソーシャル コネクタ (OSC) プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d65a8-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="d65a8-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="d65a8-105">Parameters</span></span>

<span data-ttu-id="d65a8-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="d65a8-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="d65a8-107">[in]OSC で予期される OSC プロバイダーのインターフェイスのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="d65a8-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="d65a8-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="d65a8-108">_languageTag_</span></span>
  
> <span data-ttu-id="d65a8-109">[in][[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt)と[[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt)、現在の Outlook ユーザー インターフェイスの言語を表すによって定義されているインターネット技術標準化委員会 (IETF) の言語タグ。</span><span class="sxs-lookup"><span data-stu-id="d65a8-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](http://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](http://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d65a8-110">備考</span><span class="sxs-lookup"><span data-stu-id="d65a8-110">Remarks</span></span>

<span data-ttu-id="d65a8-111">_SocialProviderInterfaceVersion_パラメーターのバージョンの形式は、 _X_です。_xxxx_、 _X_はメジャー バージョンで_xxxx_は、OSC のマイナー バージョンです。</span><span class="sxs-lookup"><span data-stu-id="d65a8-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="d65a8-112">Office 2013 では、15 の中のメジャー バージョンを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d65a8-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d65a8-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="d65a8-113">See also</span></span>

- [<span data-ttu-id="d65a8-114">ISocialProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d65a8-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

