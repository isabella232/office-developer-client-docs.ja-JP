---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433648"
---
# <a name="fbadproptag"></a><span data-ttu-id="c0cfb-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="c0cfb-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="c0cfb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0cfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0cfb-105">指定したプロパティ タグを検証します。</span><span class="sxs-lookup"><span data-stu-id="c0cfb-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c0cfb-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c0cfb-106">Header file:</span></span>  <br/> |<span data-ttu-id="c0cfb-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c0cfb-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c0cfb-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="c0cfb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c0cfb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c0cfb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c0cfb-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c0cfb-110">Called by:</span></span>  <br/> |<span data-ttu-id="c0cfb-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c0cfb-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="c0cfb-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c0cfb-112">Parameters</span></span>

 <span data-ttu-id="c0cfb-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="c0cfb-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="c0cfb-114">[in]検証するプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="c0cfb-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0cfb-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="c0cfb-115">Return value</span></span>

<span data-ttu-id="c0cfb-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c0cfb-116">TRUE</span></span> 
  
> <span data-ttu-id="c0cfb-117">指定したプロパティ タグが有効な MAPI プロパティ タグではありません。</span><span class="sxs-lookup"><span data-stu-id="c0cfb-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="c0cfb-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c0cfb-118">FALSE</span></span> 
  
> <span data-ttu-id="c0cfb-119">指定したプロパティ タグは、有効な MAPI プロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="c0cfb-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0cfb-120">注釈</span><span class="sxs-lookup"><span data-stu-id="c0cfb-120">Remarks</span></span>

<span data-ttu-id="c0cfb-121">**FBadPropTag** 関数は、MAPI 定義に基づいて指定されたプロパティ タグを検証します。</span><span class="sxs-lookup"><span data-stu-id="c0cfb-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="c0cfb-122">プロパティの種類が MAPI で定義された型の 1 つであり、プロパティ識別子がその型として定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0cfb-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0cfb-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0cfb-123">See also</span></span>



[<span data-ttu-id="c0cfb-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="c0cfb-124">FBadProp</span></span>](fbadprop.md)

