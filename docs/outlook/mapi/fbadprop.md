---
title: FBadProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadProp
api_type:
- HeaderDef
ms.assetid: 929330c8-e6f2-4adf-a36e-fba18fa055d4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2fbff399e088edaf3ad864f0ec7fecda3af6bc8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578851"
---
# <a name="fbadprop"></a><span data-ttu-id="079f9-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="079f9-103">FBadProp</span></span>

  
  
<span data-ttu-id="079f9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="079f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="079f9-105">指定されたプロパティを検証します。</span><span class="sxs-lookup"><span data-stu-id="079f9-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="079f9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="079f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="079f9-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="079f9-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="079f9-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="079f9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="079f9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="079f9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="079f9-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="079f9-110">Called by:</span></span>  <br/> |<span data-ttu-id="079f9-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="079f9-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="079f9-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="079f9-112">Parameters</span></span>

 <span data-ttu-id="079f9-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="079f9-113">_lpprop_</span></span>
  
> <span data-ttu-id="079f9-114">[in]検証するプロパティを定義する[SPropValue](spropvalue.md)構造体です。</span><span class="sxs-lookup"><span data-stu-id="079f9-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="079f9-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="079f9-115">Return value</span></span>

<span data-ttu-id="079f9-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="079f9-116">TRUE</span></span> 
  
> <span data-ttu-id="079f9-117">指定されたプロパティが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="079f9-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="079f9-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="079f9-118">FALSE</span></span> 
  
> <span data-ttu-id="079f9-119">指定したプロパティは、無効です。</span><span class="sxs-lookup"><span data-stu-id="079f9-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="079f9-120">注釈</span><span class="sxs-lookup"><span data-stu-id="079f9-120">Remarks</span></span>

<span data-ttu-id="079f9-121">サービス プロバイダーは、プロパティを設定する[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドへの呼び出しの準備など、いくつかの理由の**FBadProp**関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="079f9-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="079f9-122">**FBadProp**は、プロパティの型によって指定されたプロパティを検証します。</span><span class="sxs-lookup"><span data-stu-id="079f9-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="079f9-123">たとえば、プロパティがブール値の場合は、 **FBadProp** sures の値が TRUE または false を指定します。</span><span class="sxs-lookup"><span data-stu-id="079f9-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="079f9-124">プロパティがバイナリの場合は、 **FBadProp**のポインターとサイズを確認、正しく割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="079f9-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="079f9-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="079f9-125">See also</span></span>



[<span data-ttu-id="079f9-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="079f9-126">FBadPropTag</span></span>](fbadproptag.md)

