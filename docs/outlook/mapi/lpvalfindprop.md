---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578095"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="fc707-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="fc707-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="fc707-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc707-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc707-105">プロパティで指定したプロパティの検索を設定します。</span><span class="sxs-lookup"><span data-stu-id="fc707-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fc707-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fc707-106">Header file:</span></span>  <br/> |<span data-ttu-id="fc707-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fc707-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fc707-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="fc707-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fc707-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fc707-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fc707-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fc707-110">Called by:</span></span>  <br/> |<span data-ttu-id="fc707-111">クライアント アプリケーションとサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="fc707-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="fc707-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fc707-112">Parameters</span></span>

 <span data-ttu-id="fc707-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="fc707-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="fc707-114">[in]プロパティが、 _lpPropArray_パラメーターで指定されたプロパティ セット内で検索するタグです。</span><span class="sxs-lookup"><span data-stu-id="fc707-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="fc707-115">_あう_</span><span class="sxs-lookup"><span data-stu-id="fc707-115">_cValues_</span></span>
  
> <span data-ttu-id="fc707-116">[in]_LpPropArray_パラメーターで指定されたプロパティ セットにプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="fc707-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="fc707-117">_lpPropArray_</span><span class="sxs-lookup"><span data-stu-id="fc707-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="fc707-118">[in]検索するプロパティを定義する**SPropValue**構造体の配列。</span><span class="sxs-lookup"><span data-stu-id="fc707-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fc707-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="fc707-119">Return value</span></span>

<span data-ttu-id="fc707-120">**LpValFindProp**関数は、一致がない場合、入力プロパティのタグ、または NULL に一致するプロパティを定義する**SPropValue**構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="fc707-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fc707-121">注釈</span><span class="sxs-lookup"><span data-stu-id="fc707-121">Remarks</span></span>

<span data-ttu-id="fc707-122">**LpValFindProp**関数は、 **PpropFindProp**と同じです。</span><span class="sxs-lookup"><span data-stu-id="fc707-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc707-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc707-123">See also</span></span>



[<span data-ttu-id="fc707-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="fc707-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="fc707-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="fc707-125">SPropValue</span></span>](spropvalue.md)

