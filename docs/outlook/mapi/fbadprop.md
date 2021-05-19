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
ms.openlocfilehash: d899c8af541da231b015f6178eb7bc8f0ffd86e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426717"
---
# <a name="fbadprop"></a><span data-ttu-id="26193-103">FBadProp</span><span class="sxs-lookup"><span data-stu-id="26193-103">FBadProp</span></span>

  
  
<span data-ttu-id="26193-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26193-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26193-105">指定済みのプロパティを検証します。</span><span class="sxs-lookup"><span data-stu-id="26193-105">Validates a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26193-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="26193-106">Header file:</span></span>  <br/> |<span data-ttu-id="26193-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="26193-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="26193-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="26193-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="26193-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="26193-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="26193-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="26193-110">Called by:</span></span>  <br/> |<span data-ttu-id="26193-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="26193-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadProp(
  LPSPropValue lpprop
);
```

## <a name="parameters"></a><span data-ttu-id="26193-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="26193-112">Parameters</span></span>

 <span data-ttu-id="26193-113">_lpprop_</span><span class="sxs-lookup"><span data-stu-id="26193-113">_lpprop_</span></span>
  
> <span data-ttu-id="26193-114">[in] 検証されるプロパティを定義する [SPropValue](spropvalue.md) 構造です。</span><span class="sxs-lookup"><span data-stu-id="26193-114">[in] An [SPropValue](spropvalue.md) structure defining the property to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="26193-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="26193-115">Return value</span></span>

<span data-ttu-id="26193-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="26193-116">TRUE</span></span> 
  
> <span data-ttu-id="26193-117">指定済みのプロパティが無効です。</span><span class="sxs-lookup"><span data-stu-id="26193-117">The specified property is invalid.</span></span> 
    
<span data-ttu-id="26193-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="26193-118">FALSE</span></span> 
  
> <span data-ttu-id="26193-119">指定済みのプロパティは有効です。</span><span class="sxs-lookup"><span data-stu-id="26193-119">The specified property is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26193-120">備考</span><span class="sxs-lookup"><span data-stu-id="26193-120">Remarks</span></span>

<span data-ttu-id="26193-121">サービス プロバイダーは **FBadProp** 関数を呼び出すことができます。プロパティを設定する [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを呼び出す準備など、さまざまな用途に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="26193-121">A service provider can call the **FBadProp** function for several reasons, for example to prepare for a call to the [IMAPIProp::SetProps](imapiprop-setprops.md) method setting a property.</span></span> <span data-ttu-id="26193-122">**FBadProp** はプロパティの種類に応じて、指定済みのプロパティを検証します。</span><span class="sxs-lookup"><span data-stu-id="26193-122">**FBadProp** validates the specified property depending on the property type.</span></span> <span data-ttu-id="26193-123">たとえば、プロパティがブール値の場合、**FBadProp** は、その値が TRUE または FALSE のいずれかであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="26193-123">For example, if the property is Boolean, **FBadProp** make sures that its value is either TRUE or FALSE.</span></span> <span data-ttu-id="26193-124">プロパティがバイナリの場合は、**FBadProp** は、そのポインターおよびサイズのチェックを行い、正しく割り当てられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="26193-124">If the property is binary, **FBadProp** checks its pointer and size and makes sure that it is allocated correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26193-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="26193-125">See also</span></span>



[<span data-ttu-id="26193-126">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="26193-126">FBadPropTag</span></span>](fbadproptag.md)

