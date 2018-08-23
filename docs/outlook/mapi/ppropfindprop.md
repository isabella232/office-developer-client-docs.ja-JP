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
ms.openlocfilehash: b7755f2ec067003e47d358a9736c6d7d96ede267
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803696"
---
# <a name="ppropfindprop"></a><span data-ttu-id="c979c-103">PpropFindProp</span><span class="sxs-lookup"><span data-stu-id="c979c-103">PpropFindProp</span></span>

  
  
<span data-ttu-id="c979c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c979c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c979c-105">プロパティで指定したプロパティの検索を設定します。</span><span class="sxs-lookup"><span data-stu-id="c979c-105">Searches for a specified property in a property set.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c979c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c979c-106">Header file:</span></span>  <br/> |<span data-ttu-id="c979c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c979c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c979c-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="c979c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c979c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c979c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c979c-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c979c-110">Called by:</span></span>  <br/> |<span data-ttu-id="c979c-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c979c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="c979c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c979c-112">Parameters</span></span>

 <span data-ttu-id="c979c-113">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="c979c-113">_rgprop_</span></span>
  
> <span data-ttu-id="c979c-114">[in]検索するプロパティを定義する[SPropValue](spropvalue.md)構造体の配列です。</span><span class="sxs-lookup"><span data-stu-id="c979c-114">[in] Array of [SPropValue](spropvalue.md) structures that define the properties to be searched.</span></span> 
    
 <span data-ttu-id="c979c-115">_cprop_</span><span class="sxs-lookup"><span data-stu-id="c979c-115">_cprop_</span></span>
  
> <span data-ttu-id="c979c-116">[in]_Rgprop_パラメーターで指定されたプロパティ セット内のプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="c979c-116">[in] Count of properties in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="c979c-117">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="c979c-117">_ulPropTag_</span></span>
  
> <span data-ttu-id="c979c-118">[in]_Rgprop_パラメーターで指定されたプロパティ セット内で検索するプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="c979c-118">[in] Property tag for the property to search for in the property set indicated by the  _rgprop_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c979c-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="c979c-119">Return value</span></span>

 <span data-ttu-id="c979c-120">**PpropFindProp**は、一致がない場合、入力プロパティのタグ、または NULL に一致するプロパティを定義する、 [SPropValue](spropvalue.md)構造体を返します。</span><span class="sxs-lookup"><span data-stu-id="c979c-120">**PpropFindProp** returns an [SPropValue](spropvalue.md) structure defining the property that matches the input property tag, or NULL if there is no match.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c979c-121">注釈</span><span class="sxs-lookup"><span data-stu-id="c979c-121">Remarks</span></span>

<span data-ttu-id="c979c-122">プロパティを指定したタグには、PT_UNSPECIFIED の種類のプロパティが示されている場合**PpropFindProp**関数は、タグにプロパティの識別子にのみ一致するものを検索します。</span><span class="sxs-lookup"><span data-stu-id="c979c-122">If the given property tag indicates a property of type PT_UNSPECIFIED, the **PpropFindProp** function finds a match only for the property identifier in the tag.</span></span> <span data-ttu-id="c979c-123">それ以外の場合、プロパティの型を含め、全体のプロパティ タグの一致を検出し、識別されるプロパティを返します。</span><span class="sxs-lookup"><span data-stu-id="c979c-123">Otherwise, it finds a match for the entire property tag, including the property type, and returns the property identified.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c979c-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="c979c-124">MFCMAPI reference</span></span>

<span data-ttu-id="c979c-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="c979c-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c979c-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="c979c-126">**File**</span></span>|<span data-ttu-id="c979c-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="c979c-127">**Function**</span></span>|<span data-ttu-id="c979c-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="c979c-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c979c-129">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="c979c-129">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="c979c-130">CContentsTableListCtrl::BuildDataItem</span><span class="sxs-lookup"><span data-stu-id="c979c-130">CContentsTableListCtrl::BuildDataItem</span></span>  <br/> |<span data-ttu-id="c979c-131">MFCMAPI では、 **PpropFindProp**メソッドを使用して、リストに追加されているプロパティのプロパティの設定を検索します。</span><span class="sxs-lookup"><span data-stu-id="c979c-131">MFCMAPI uses the **PpropFindProp** method to find properties in a property set being added to the list.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c979c-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="c979c-132">See also</span></span>



<span data-ttu-id="c979c-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c979c-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

