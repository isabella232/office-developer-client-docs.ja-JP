---
title: FBadPropTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadPropTag
api_type:
- HeaderDef
ms.assetid: 143bd3c6-5a55-4122-8522-9c48473aa781
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 943dab0141581adc32c184b0042a063a4ec05c3e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582883"
---
# <a name="fbadproptag"></a><span data-ttu-id="79927-103">FBadPropTag</span><span class="sxs-lookup"><span data-stu-id="79927-103">FBadPropTag</span></span>

  
  
<span data-ttu-id="79927-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79927-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79927-105">指定されたプロパティ タグを検証します。</span><span class="sxs-lookup"><span data-stu-id="79927-105">Validates a specified property tag.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79927-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="79927-106">Header file:</span></span>  <br/> |<span data-ttu-id="79927-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="79927-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="79927-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="79927-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="79927-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="79927-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="79927-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="79927-110">Called by:</span></span>  <br/> |<span data-ttu-id="79927-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="79927-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadPropTag(
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="79927-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="79927-112">Parameters</span></span>

 <span data-ttu-id="79927-113">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="79927-113">_ulPropTag_</span></span>
  
> <span data-ttu-id="79927-114">[in]検証するプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="79927-114">[in] The property tag to be validated.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="79927-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="79927-115">Return value</span></span>

<span data-ttu-id="79927-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="79927-116">TRUE</span></span> 
  
> <span data-ttu-id="79927-117">指定されたプロパティ タグは、有効な MAPI プロパティ タグではありません。</span><span class="sxs-lookup"><span data-stu-id="79927-117">The specified property tag is not a valid MAPI property tag.</span></span> 
    
<span data-ttu-id="79927-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="79927-118">FALSE</span></span> 
  
> <span data-ttu-id="79927-119">指定されたプロパティ タグは、有効な MAPI プロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="79927-119">The specified property tag is a valid MAPI property tag.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79927-120">注釈</span><span class="sxs-lookup"><span data-stu-id="79927-120">Remarks</span></span>

<span data-ttu-id="79927-121">**FBadPropTag**関数では、MAPI 定義に基づいて、指定されたプロパティ タグを検証します。</span><span class="sxs-lookup"><span data-stu-id="79927-121">The **FBadPropTag** function validates the specified property tag based on MAPI definitions.</span></span> <span data-ttu-id="79927-122">Sures プロパティの型は、MAPI によって定義された型のいずれかをその型のプロパティの識別子が定義されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="79927-122">It make sures that the property type is one of the types defined by MAPI and that the property identifier is defined to be of that type.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79927-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="79927-123">See also</span></span>



[<span data-ttu-id="79927-124">FBadProp</span><span class="sxs-lookup"><span data-stu-id="79927-124">FBadProp</span></span>](fbadprop.md)

