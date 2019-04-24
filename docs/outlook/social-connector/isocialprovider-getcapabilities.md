---
title: i、alprovidergetcapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: プロバイダー機能について説明する文字列を取得します。
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285765"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="5522b-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="5522b-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="5522b-104">プロバイダー機能について説明する文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="5522b-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="5522b-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5522b-105">Parameters</span></span>

<span data-ttu-id="5522b-106">_result_</span><span class="sxs-lookup"><span data-stu-id="5522b-106">_result_</span></span>
  
> <span data-ttu-id="5522b-107">読み上げOutlook Social Connector (.osc) プロバイダーの機能を表す XML 文字列。</span><span class="sxs-lookup"><span data-stu-id="5522b-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5522b-108">解説</span><span class="sxs-lookup"><span data-stu-id="5522b-108">Remarks</span></span>

<span data-ttu-id="5522b-109">返された_結果_xml 文字列は、**機能**要素のスキーマ定義に準拠している必要があります。そのためには、プロバイダ拡張用の XML スキーマで定義されています。</span><span class="sxs-lookup"><span data-stu-id="5522b-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="5522b-110">プロバイダーは、_結果_の文字列を返して、.osc からプロバイダーへの後続の呼び出しが正しく動作するようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5522b-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5522b-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="5522b-111">See also</span></span>

- [<span data-ttu-id="5522b-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5522b-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

