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
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804352"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="c2f32-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="c2f32-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="c2f32-104">プロバイダーの機能を説明する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="c2f32-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="c2f32-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c2f32-105">Parameters</span></span>

<span data-ttu-id="c2f32-106">_result_</span><span class="sxs-lookup"><span data-stu-id="c2f32-106">_result_</span></span>
  
> <span data-ttu-id="c2f32-107">[out]Outlook ソーシャル コネクタ (OSC) プロバイダーの機能を表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="c2f32-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2f32-108">注釈</span><span class="sxs-lookup"><span data-stu-id="c2f32-108">Remarks</span></span>

<span data-ttu-id="c2f32-109">返される_結果_の XML 文字列は、OSC プロバイダーの拡張機能の XML スキーマで定義されている**機能**要素のスキーマ定義に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2f32-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="c2f32-110">プロバイダーでは、以降、OSC からプロバイダーに正常に動作するを有効にするのには_結果_の文字列を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2f32-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2f32-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="c2f32-111">See also</span></span>

- [<span data-ttu-id="c2f32-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2f32-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

