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
ms.openlocfilehash: 7bcaf230eed9cf21388b68f06ab678dc143f64ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571823"
---
# <a name="proptype"></a><span data-ttu-id="3884a-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="3884a-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="3884a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3884a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3884a-105">指定されたプロパティ タグのプロパティの型を返します。</span><span class="sxs-lookup"><span data-stu-id="3884a-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3884a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3884a-106">Header file:</span></span>  <br/> |<span data-ttu-id="3884a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3884a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3884a-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="3884a-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="3884a-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3884a-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="3884a-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3884a-110">Parameters</span></span>

 <span data-ttu-id="3884a-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="3884a-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="3884a-112">プロパティ タグを取得するプロパティの型が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3884a-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3884a-113">注釈</span><span class="sxs-lookup"><span data-stu-id="3884a-113">Remarks</span></span>

<span data-ttu-id="3884a-114">プロパティの種類を調べるには、 **PROP_TYPE**マクロを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3884a-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="3884a-115">PT_BINARY が返される値の PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) の結果を呼び出すなどです。</span><span class="sxs-lookup"><span data-stu-id="3884a-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="3884a-116">プロパティのすべてのタグには、下位ワード (ビット 0 ~ 15) のプロパティの型と、上位ワード (16 ~ 31 のビット) のプロパティの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3884a-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="3884a-117">**PROP_TYPE**マクロは、プロパティの型を抽出し返される整数の 15 からビット 0 に配置します。</span><span class="sxs-lookup"><span data-stu-id="3884a-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="3884a-118">戻り値の残りのビットは、0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="3884a-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3884a-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="3884a-119">See also</span></span>



[<span data-ttu-id="3884a-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3884a-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="3884a-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="3884a-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

