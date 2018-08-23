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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e9ad675e6df88265238a28f18e5cfcdacfdfbb5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803985"
---
# <a name="spropattrarray"></a><span data-ttu-id="d3afa-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="d3afa-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="d3afa-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3afa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3afa-105">オブジェクトのプロパティの属性の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3afa-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3afa-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d3afa-106">Header file:</span></span>  <br/> |<span data-ttu-id="d3afa-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="d3afa-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="d3afa-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="d3afa-108">Related macros:</span></span>  <br/> |<span data-ttu-id="d3afa-109">[CbNewSPropAttrArray](cbnewspropattrarray.md)、 [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="d3afa-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="d3afa-110">Members</span><span class="sxs-lookup"><span data-stu-id="d3afa-110">Members</span></span>

 <span data-ttu-id="d3afa-111">**あう**</span><span class="sxs-lookup"><span data-stu-id="d3afa-111">**cValues**</span></span>
  
> <span data-ttu-id="d3afa-112">**APropAttr**メンバーのプロパティの属性の数。</span><span class="sxs-lookup"><span data-stu-id="d3afa-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="d3afa-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="d3afa-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="d3afa-114">プロパティの属性の配列。</span><span class="sxs-lookup"><span data-stu-id="d3afa-114">An array of property attributes.</span></span> <span data-ttu-id="d3afa-115">属性の有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d3afa-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="d3afa-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="d3afa-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="d3afa-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="d3afa-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="d3afa-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="d3afa-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="d3afa-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="d3afa-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3afa-120">注釈</span><span class="sxs-lookup"><span data-stu-id="d3afa-120">Remarks</span></span>

<span data-ttu-id="d3afa-121">**SPropAttrArray**構造体を使用して実装されているデータ オブジェクトのプロパティで、 [IPropData: IMAPIProp](ipropdataimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="d3afa-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="d3afa-122">MAPI の実装で使用されても[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)に基づいて構造化ストレージは。</span><span class="sxs-lookup"><span data-stu-id="d3afa-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d3afa-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="d3afa-123">See also</span></span>



[<span data-ttu-id="d3afa-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d3afa-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="d3afa-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3afa-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="d3afa-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="d3afa-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="d3afa-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="d3afa-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="d3afa-128">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="d3afa-128">MAPI Structures</span></span>](mapi-structures.md)

