---
title: PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_TYPE
api_type:
- COM
ms.assetid: 746d63fa-bfb7-479f-94dc-ba40011c1ec9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412836"
---
# <a name="prop_type"></a><span data-ttu-id="69b77-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="69b77-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="69b77-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69b77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69b77-105">指定したプロパティ タグのプロパティの種類を返します。</span><span class="sxs-lookup"><span data-stu-id="69b77-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="69b77-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="69b77-106">Header file:</span></span>  <br/> |<span data-ttu-id="69b77-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69b77-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="69b77-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="69b77-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="69b77-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="69b77-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="69b77-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="69b77-110">Parameters</span></span>

 <span data-ttu-id="69b77-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="69b77-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="69b77-112">返されるプロパティの種類を含むプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="69b77-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="69b77-113">注釈</span><span class="sxs-lookup"><span data-stu-id="69b77-113">Remarks</span></span>

<span data-ttu-id="69b77-114">プロパティ **PROP_TYPE** マクロを使用して、プロパティの種類を特定できます。</span><span class="sxs-lookup"><span data-stu-id="69b77-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="69b77-115">たとえば、呼び出PROP_TYPE **(** PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md))) は、返される値PT_BINARYします。</span><span class="sxs-lookup"><span data-stu-id="69b77-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="69b77-116">すべてのプロパティ タグには、低次ワード (ビット 0 ~ 15) のプロパティ型と、高次ワード (ビット 16 ~ 31) のプロパティ識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="69b77-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="69b77-117">この **PROP_TYPE** は、プロパティの種類を抽出し、返される整数のビット 0 ~ 15 に格納します。</span><span class="sxs-lookup"><span data-stu-id="69b77-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="69b77-118">戻り値の残りのビットは 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="69b77-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="69b77-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="69b77-119">See also</span></span>



[<span data-ttu-id="69b77-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="69b77-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="69b77-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="69b77-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

