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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9764be2788db8d2649be8708cad4ec67a85af845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341000"
---
# <a name="fbadproptag"></a><span data-ttu-id="d9520-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="d9520-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="d9520-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9520-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9520-105">指定されたプロパティタグを検証します。</span><span class="sxs-lookup"><span data-stu-id="d9520-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d9520-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d9520-106">Header file:</span></span>  <br/> |<span data-ttu-id="d9520-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="d9520-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="d9520-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="d9520-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d9520-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d9520-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d9520-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d9520-110">Called by:</span></span>  <br/> |<span data-ttu-id="d9520-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d9520-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="d9520-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9520-112">Parameters</span></span>

 <span data-ttu-id="d9520-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="d9520-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="d9520-114">順番検証するプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="d9520-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9520-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9520-115">Return value</span></span>

<span data-ttu-id="d9520-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="d9520-116">TRUE</span></span> 
  
> <span data-ttu-id="d9520-117">指定されたプロパティタグは、有効な MAPI プロパティタグではありません。</span><span class="sxs-lookup"><span data-stu-id="d9520-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="d9520-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="d9520-118">FALSE</span></span> 
  
> <span data-ttu-id="d9520-119">指定されたプロパティタグは、有効な MAPI プロパティタグです。</span><span class="sxs-lookup"><span data-stu-id="d9520-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9520-120">解説</span><span class="sxs-lookup"><span data-stu-id="d9520-120">Remarks</span></span>

<span data-ttu-id="d9520-121">**FBadPropTag**関数は、MAPI 定義に基づいて指定されたプロパティタグを検証します。</span><span class="sxs-lookup"><span data-stu-id="d9520-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="d9520-122">プロパティの型が MAPI で定義されている型の1つであり、プロパティ識別子がその型に定義されていることを sures にします。</span><span class="sxs-lookup"><span data-stu-id="d9520-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9520-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9520-123">See also</span></span>



[<span data-ttu-id="d9520-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="d9520-124">FBadProp</span></span>](fbadprop.md)

