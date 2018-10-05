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
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385831"
---
# <a name="isocialproviderload"></a><span data-ttu-id="77ac6-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="77ac6-103">ISocialProvider::Load</span></span>

<span data-ttu-id="77ac6-104">Outlook ソーシャル コネクタ (OSC) プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="77ac6-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="77ac6-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="77ac6-105">Parameters</span></span>

<span data-ttu-id="77ac6-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="77ac6-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="77ac6-107">[in]OSC で予期される OSC プロバイダーのインターフェイスのバージョンです。</span><span class="sxs-lookup"><span data-stu-id="77ac6-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="77ac6-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="77ac6-108">_languageTag_</span></span>
  
> <span data-ttu-id="77ac6-109">[in][[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt)と[[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)、現在の Outlook ユーザー インターフェイスの言語を表すによって定義されているインターネット技術標準化委員会 (IETF) の言語タグ。</span><span class="sxs-lookup"><span data-stu-id="77ac6-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77ac6-110">備考</span><span class="sxs-lookup"><span data-stu-id="77ac6-110">Remarks</span></span>

<span data-ttu-id="77ac6-111">_SocialProviderInterfaceVersion_パラメーターのバージョンの形式は、 _X_です。_xxxx_、 _X_はメジャー バージョンで_xxxx_は、OSC のマイナー バージョンです。</span><span class="sxs-lookup"><span data-stu-id="77ac6-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="77ac6-112">Office 2013 では、15 の中のメジャー バージョンを確認してください。</span><span class="sxs-lookup"><span data-stu-id="77ac6-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77ac6-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="77ac6-113">See also</span></span>

- [<span data-ttu-id="77ac6-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77ac6-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

