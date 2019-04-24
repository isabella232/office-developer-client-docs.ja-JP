---
title: i、alproviderload
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Outlook Social Connector (.osc) プロバイダーを初期化します。
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285760"
---
# <a name="isocialproviderload"></a><span data-ttu-id="e2ede-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="e2ede-103">ISocialProvider::Load</span></span>

<span data-ttu-id="e2ede-104">Outlook Social Connector (.osc) プロバイダーを初期化します。</span><span class="sxs-lookup"><span data-stu-id="e2ede-104">Initializes the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="e2ede-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2ede-105">Parameters</span></span>

<span data-ttu-id="e2ede-106">_このバージョンの形式_</span><span class="sxs-lookup"><span data-stu-id="e2ede-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="e2ede-107">順番.osc が想定する .osc プロバイダインターフェイスのバージョン。</span><span class="sxs-lookup"><span data-stu-id="e2ede-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="e2ede-108">_言語タグ_</span><span class="sxs-lookup"><span data-stu-id="e2ede-108">_languageTag_</span></span>
  
> <span data-ttu-id="e2ede-109">順番[[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt)および[[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt)で定義されている、現在の Outlook ユーザーインターフェイス言語を表すインターネット技術標準化委員会 (IETF) 言語タグ。</span><span class="sxs-lookup"><span data-stu-id="e2ede-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2ede-110">解説</span><span class="sxs-lookup"><span data-stu-id="e2ede-110">Remarks</span></span>

<span data-ttu-id="e2ede-111">指定されたパラメーター __ のバージョンは_X_です。_xxxx_。ここで、 _X_はメジャーバージョン、 _xxxx_は .osc のマイナーバージョンです。</span><span class="sxs-lookup"><span data-stu-id="e2ede-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="e2ede-112">Office 2013 の場合は、メジャーバージョンが15であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="e2ede-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2ede-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2ede-113">See also</span></span>

- [<span data-ttu-id="e2ede-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2ede-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

