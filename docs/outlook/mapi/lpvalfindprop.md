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
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357429"
---
# <a name="lpvalfindprop"></a><span data-ttu-id="c72ab-103">LpValFindProp</span><span class="sxs-lookup"><span data-stu-id="c72ab-103">LpValFindProp</span></span>

  
  
<span data-ttu-id="c72ab-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c72ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c72ab-105">プロパティセット内の指定されたプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="c72ab-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c72ab-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c72ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="c72ab-107">mapiutil</span><span class="sxs-lookup"><span data-stu-id="c72ab-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c72ab-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="c72ab-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c72ab-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c72ab-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c72ab-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c72ab-110">Called by:</span></span>  <br/> |<span data-ttu-id="c72ab-111">クライアントアプリケーションとサービスプロバイダー。</span><span class="sxs-lookup"><span data-stu-id="c72ab-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a><span data-ttu-id="c72ab-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c72ab-112">Parameters</span></span>

 <span data-ttu-id="c72ab-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="c72ab-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="c72ab-114">順番タグを指定します。このプロパティは、 _lpproparray_パラメーターで示されます。</span><span class="sxs-lookup"><span data-stu-id="c72ab-114">[in] Tag for the property to search for in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="c72ab-115">_cvalues_</span><span class="sxs-lookup"><span data-stu-id="c72ab-115">_cValues_</span></span>
  
> <span data-ttu-id="c72ab-116">順番_lpproparray_パラメーターで示される、プロパティセット内のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="c72ab-116">[in] Count of properties in the property set, indicated by the  _lpPropArray_ parameter.</span></span> 
    
 <span data-ttu-id="c72ab-117">_lpproparray_</span><span class="sxs-lookup"><span data-stu-id="c72ab-117">_lpPropArray_</span></span>
  
> <span data-ttu-id="c72ab-118">順番検索するプロパティを定義する**spropvalue**構造の配列です。</span><span class="sxs-lookup"><span data-stu-id="c72ab-118">[in] Array of **SPropValue** structures that defines the properties to be searched.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c72ab-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="c72ab-119">Return value</span></span>

<span data-ttu-id="c72ab-120">**lpvalfindprop**関数は、入力プロパティタグに一致するプロパティを定義する**spropvalue**構造体を返します。一致しない場合は NULL になります。</span><span class="sxs-lookup"><span data-stu-id="c72ab-120">The **LpValFindProp** function returns an **SPropValue** structure that defines the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c72ab-121">解説</span><span class="sxs-lookup"><span data-stu-id="c72ab-121">Remarks</span></span>

<span data-ttu-id="c72ab-122">**lpvalfindprop**関数は、 **ppropfindprop**と同じです。</span><span class="sxs-lookup"><span data-stu-id="c72ab-122">The **LpValFindProp** function is identical to **PpropFindProp**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c72ab-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="c72ab-123">See also</span></span>



[<span data-ttu-id="c72ab-124">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="c72ab-124">PpropFindProp</span></span>](ppropfindprop.md)
  
[<span data-ttu-id="c72ab-125">SPropValue</span><span class="sxs-lookup"><span data-stu-id="c72ab-125">SPropValue</span></span>](spropvalue.md)

