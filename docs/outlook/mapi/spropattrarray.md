---
title: SPropAttrArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropAttrArray
api_type:
- COM
ms.assetid: 30dd19d9-0840-49e9-aec6-ec8d19b1f91d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 55cba4f7cfb3fa8035117348b10ab1d6d3082710
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405514"
---
# <a name="spropattrarray"></a><span data-ttu-id="76b89-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="76b89-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="76b89-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76b89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76b89-105">オブジェクトのプロパティの属性の一覧を含む。</span><span class="sxs-lookup"><span data-stu-id="76b89-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76b89-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="76b89-106">Header file:</span></span>  <br/> |<span data-ttu-id="76b89-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="76b89-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="76b89-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="76b89-108">Related macros:</span></span>  <br/> |<span data-ttu-id="76b89-109">[CbNewSPropAttrArray](cbnewspropattrarray.md)、 [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="76b89-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="76b89-110">Members</span><span class="sxs-lookup"><span data-stu-id="76b89-110">Members</span></span>

 <span data-ttu-id="76b89-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="76b89-111">**cValues**</span></span>
  
> <span data-ttu-id="76b89-112">**aPropAttr メンバーのプロパティ属性の** 数。</span><span class="sxs-lookup"><span data-stu-id="76b89-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="76b89-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="76b89-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="76b89-114">プロパティ属性の配列。</span><span class="sxs-lookup"><span data-stu-id="76b89-114">An array of property attributes.</span></span> <span data-ttu-id="76b89-115">属性の有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="76b89-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="76b89-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="76b89-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="76b89-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="76b89-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="76b89-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="76b89-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="76b89-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="76b89-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76b89-120">注釈</span><span class="sxs-lookup"><span data-stu-id="76b89-120">Remarks</span></span>

<span data-ttu-id="76b89-121">**SPropAttrArray** 構造体は [、IPropData : IMAPIProp](ipropdataimapiprop.md)インターフェイスを実装するプロパティ データ オブジェクトによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="76b89-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="76b89-122">また、MAPI の [IMAPIMessageSite : 構造化](imapimessagesiteiunknown.md) ストレージに基づく IUnknown の実装でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="76b89-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76b89-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="76b89-123">See also</span></span>



[<span data-ttu-id="76b89-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="76b89-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="76b89-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76b89-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="76b89-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="76b89-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="76b89-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="76b89-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="76b89-128">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="76b89-128">MAPI Structures</span></span>](mapi-structures.md)

