---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350732"
---
# <a name="ppropfindprop"></a><span data-ttu-id="607b7-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="607b7-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="607b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="607b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="607b7-105">プロパティセット内の指定されたプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="607b7-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="607b7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="607b7-106">Header file:</span></span>  <br/> |<span data-ttu-id="607b7-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="607b7-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="607b7-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="607b7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="607b7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="607b7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="607b7-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="607b7-110">Called by:</span></span>  <br/> |<span data-ttu-id="607b7-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="607b7-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="607b7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="607b7-112">Parameters</span></span>

 <span data-ttu-id="607b7-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="607b7-113">_rgprop_</span></span>
  
> <span data-ttu-id="607b7-114">順番検索するプロパティを定義する[spropvalue](spropvalue.md)構造の配列です。</span><span class="sxs-lookup"><span data-stu-id="607b7-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="607b7-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="607b7-115">_cprop_</span></span>
  
> <span data-ttu-id="607b7-116">順番_rgprop_パラメーターによって示されるプロパティセット内のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="607b7-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="607b7-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="607b7-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="607b7-118">順番_rgprop_パラメーターによって示されるプロパティセット内で検索するプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="607b7-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="607b7-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="607b7-119">Return value</span></span>

 <span data-ttu-id="607b7-120">**ppropfindprop**は、入力プロパティタグに一致するプロパティを定義する[spropvalue](spropvalue.md)構造体を返します。一致しない場合は NULL になります。</span><span class="sxs-lookup"><span data-stu-id="607b7-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="607b7-121">解説</span><span class="sxs-lookup"><span data-stu-id="607b7-121">Remarks</span></span>

<span data-ttu-id="607b7-122">指定したプロパティタグが PT_UNSPECIFIED 型のプロパティを示している場合、 **ppropfindprop**関数は、タグ内のプロパティ識別子に対してのみ一致を検出します。</span><span class="sxs-lookup"><span data-stu-id="607b7-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="607b7-123">それ以外の場合は、プロパティの型を含む property タグ全体の一致を検索し、識別されたプロパティを返します。</span><span class="sxs-lookup"><span data-stu-id="607b7-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="607b7-124">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="607b7-124">MFCMAPI reference</span></span>

<span data-ttu-id="607b7-125">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="607b7-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="607b7-126">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="607b7-126">**File**</span></span>|<span data-ttu-id="607b7-127">**関数**</span><span class="sxs-lookup"><span data-stu-id="607b7-127">**Function**</span></span>|<span data-ttu-id="607b7-128">**コメント**</span><span class="sxs-lookup"><span data-stu-id="607b7-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="607b7-129">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="607b7-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="607b7-130">CContentsTableListCtrl:: builddataitem</span><span class="sxs-lookup"><span data-stu-id="607b7-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="607b7-131">mfcmapi は、 **ppropfindprop**メソッドを使用して、リストに追加されているプロパティセット内のプロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="607b7-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="607b7-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="607b7-132">See also</span></span>



<span data-ttu-id="607b7-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="607b7-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

