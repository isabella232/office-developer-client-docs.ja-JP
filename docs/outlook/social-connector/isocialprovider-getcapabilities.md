---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: プロバイダーの機能を説明する文字列を取得します。
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408104"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="c876a-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="c876a-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="c876a-104">プロバイダーの機能を説明する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="c876a-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="c876a-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c876a-105">Parameters</span></span>

<span data-ttu-id="c876a-106">_result_</span><span class="sxs-lookup"><span data-stu-id="c876a-106">_result_</span></span>
  
> <span data-ttu-id="c876a-107">[out]ソーシャル コネクタ (OSC) プロバイダーの機能Outlook XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="c876a-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c876a-108">注釈</span><span class="sxs-lookup"><span data-stu-id="c876a-108">Remarks</span></span>

<span data-ttu-id="c876a-109">返  _される結果_ XML 文字列は、OSC プロバイダーの機能拡張のための XML スキーマで定義されている **、capabilities** 要素のスキーマ定義に準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="c876a-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="c876a-110">プロバイダーは、OSC  _からプロバイダー_ への後続の呼び出しが正しく動作するように、結果文字列を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c876a-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c876a-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="c876a-111">See also</span></span>

- [<span data-ttu-id="c876a-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c876a-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

