---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d7601eb50818fa6f39384a6b024215fc4917e83a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801281"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="f213d-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="f213d-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="f213d-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f213d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f213d-105">プロパティで指定したプロパティの検索を設定します。</span><span class="sxs-lookup"><span data-stu-id="f213d-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f213d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f213d-106">Header file:</span></span>  <br/> |<span data-ttu-id="f213d-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f213d-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f213d-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f213d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f213d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f213d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f213d-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f213d-110">Called by:</span></span>  <br/> |<span data-ttu-id="f213d-111">クライアント アプリケーションとサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="f213d-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="f213d-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f213d-112">Parameters</span></span>

 <span data-ttu-id="f213d-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="f213d-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="f213d-114">[in]プロパティが、 _lpPropArray_パラメーターで指定されたプロパティ セット内で検索するタグです。</span><span class="sxs-lookup"><span data-stu-id="f213d-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="f213d-115">_あう_</span><span class="sxs-lookup"><span data-stu-id="f213d-115">_cValues_</span></span>
  
> <span data-ttu-id="f213d-116">[in]_LpPropArray_パラメーターで指定されたプロパティ セットにプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="f213d-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="f213d-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="f213d-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="f213d-118">[in]検索するプロパティを定義する**SPropValue**構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="f213d-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f213d-119">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f213d-119">Return value</span></span>

<span data-ttu-id="f213d-120">**LpValFindProp**関数は、一致がない場合、入力プロパティのタグ、または NULL に一致するプロパティを定義する**SPropValue**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="f213d-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f213d-121">備考</span><span class="sxs-lookup"><span data-stu-id="f213d-121">Remarks</span></span>

<span data-ttu-id="f213d-122">**LpValFindProp**関数は、 **PpropFindProp**と同じです。</span><span class="sxs-lookup"><span data-stu-id="f213d-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f213d-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f213d-123">See also</span></span>



[<span data-ttu-id="f213d-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="f213d-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="f213d-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f213d-125">SPropValue</span></span>](spropvalue.md)

