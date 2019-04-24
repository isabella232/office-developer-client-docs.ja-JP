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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c33633c4decd697cf241f8b7c27360f776a1ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332761"
---
# <a name="proptype"></a><span data-ttu-id="30eea-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="30eea-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="30eea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30eea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30eea-105">指定したプロパティタグのプロパティの種類を返します。</span><span class="sxs-lookup"><span data-stu-id="30eea-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30eea-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="30eea-106">Header file:</span></span>  <br/> |<span data-ttu-id="30eea-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="30eea-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="30eea-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="30eea-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="30eea-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="30eea-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="30eea-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="30eea-110">Parameters</span></span>

 <span data-ttu-id="30eea-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="30eea-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="30eea-112">返されるプロパティの型を含む property タグ。</span><span class="sxs-lookup"><span data-stu-id="30eea-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="30eea-113">解説</span><span class="sxs-lookup"><span data-stu-id="30eea-113">Remarks</span></span>

<span data-ttu-id="30eea-114">**PROP_TYPE**マクロを使用して、プロパティの種類を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="30eea-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="30eea-115">たとえば、PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) を呼び出すと、値 PT_BINARY が返されます。</span><span class="sxs-lookup"><span data-stu-id="30eea-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="30eea-116">すべてのプロパティタグには、下位ワード (ビット 0 ~ 15) のプロパティの種類と、上位ワード (ビット 16 ~ 31) のプロパティの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="30eea-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="30eea-117">**PROP_TYPE**マクロは、プロパティの型を抽出し、それをビット 0 ~ 15 の整数に設定して返します。</span><span class="sxs-lookup"><span data-stu-id="30eea-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="30eea-118">戻り値の残りのビットは0に設定されます。</span><span class="sxs-lookup"><span data-stu-id="30eea-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30eea-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="30eea-119">See also</span></span>



[<span data-ttu-id="30eea-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="30eea-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="30eea-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="30eea-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

