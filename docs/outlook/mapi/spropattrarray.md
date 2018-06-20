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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e9ad675e6df88265238a28f18e5cfcdacfdfbb5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803985"
---
# <a name="spropattrarray"></a><span data-ttu-id="cccd5-103">SPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="cccd5-103">SPropAttrArray</span></span>

  
  
<span data-ttu-id="cccd5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cccd5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cccd5-105">オブジェクトのプロパティの属性の一覧が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cccd5-105">Contains a list of attributes for properties of an object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cccd5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cccd5-106">Header file:</span></span>  <br/> |<span data-ttu-id="cccd5-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="cccd5-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="cccd5-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="cccd5-108">Related macros:</span></span>  <br/> |<span data-ttu-id="cccd5-109">[CbNewSPropAttrArray](cbnewspropattrarray.md)、 [CbSPropAttrArray](cbspropattrarray.md)</span><span class="sxs-lookup"><span data-stu-id="cccd5-109">[CbNewSPropAttrArray](cbnewspropattrarray.md), [CbSPropAttrArray](cbspropattrarray.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cValues;
  ULONG aPropAttr[MAPI_DIM];
} SPropAttrArray, FAR *LPSPropAttrArray;

```

## <a name="members"></a><span data-ttu-id="cccd5-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="cccd5-110">Members</span></span>

 <span data-ttu-id="cccd5-111">**あう**</span><span class="sxs-lookup"><span data-stu-id="cccd5-111">**cValues**</span></span>
  
> <span data-ttu-id="cccd5-112">**APropAttr**メンバーのプロパティの属性の数。</span><span class="sxs-lookup"><span data-stu-id="cccd5-112">Count of property attributes in the **aPropAttr** member.</span></span> 
    
 <span data-ttu-id="cccd5-113">**aPropAttr**</span><span class="sxs-lookup"><span data-stu-id="cccd5-113">**aPropAttr**</span></span>
  
> <span data-ttu-id="cccd5-114">プロパティの属性の配列。</span><span class="sxs-lookup"><span data-stu-id="cccd5-114">An array of property attributes.</span></span> <span data-ttu-id="cccd5-115">属性の有効な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cccd5-115">Valid values for attributes are as follows:</span></span>
    
    - <span data-ttu-id="cccd5-116">PROPATTR_MANDATORY</span><span class="sxs-lookup"><span data-stu-id="cccd5-116">PROPATTR_MANDATORY</span></span>
    
    - <span data-ttu-id="cccd5-117">PROPATTR_READABLE</span><span class="sxs-lookup"><span data-stu-id="cccd5-117">PROPATTR_READABLE</span></span>
    
    - <span data-ttu-id="cccd5-118">PROPATTR_WRITEABLE</span><span class="sxs-lookup"><span data-stu-id="cccd5-118">PROPATTR_WRITEABLE</span></span>
    
    - <span data-ttu-id="cccd5-119">PROPATTR_NOT_PRESENT</span><span class="sxs-lookup"><span data-stu-id="cccd5-119">PROPATTR_NOT_PRESENT</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cccd5-120">備考</span><span class="sxs-lookup"><span data-stu-id="cccd5-120">Remarks</span></span>

<span data-ttu-id="cccd5-121">**SPropAttrArray**構造体を使用して実装されているデータ オブジェクトのプロパティで、 [IPropData: IMAPIProp](ipropdataimapiprop.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="cccd5-121">The **SPropAttrArray** structure is used by property data objects that implement the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> <span data-ttu-id="cccd5-122">MAPI の実装で使用されても[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)に基づいて構造化ストレージは。</span><span class="sxs-lookup"><span data-stu-id="cccd5-122">It is also used by MAPI's implementation of [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) that is based on structured storage.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cccd5-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="cccd5-123">See also</span></span>



[<span data-ttu-id="cccd5-124">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="cccd5-124">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)
  
[<span data-ttu-id="cccd5-125">IMAPIMessageSite: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cccd5-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)
  
[<span data-ttu-id="cccd5-126">CbNewSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="cccd5-126">CbNewSPropAttrArray</span></span>](cbnewspropattrarray.md)
  
[<span data-ttu-id="cccd5-127">CbSPropAttrArray</span><span class="sxs-lookup"><span data-stu-id="cccd5-127">CbSPropAttrArray</span></span>](cbspropattrarray.md)


[<span data-ttu-id="cccd5-128">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="cccd5-128">MAPI Structures</span></span>](mapi-structures.md)

