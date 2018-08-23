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
ms.openlocfilehash: 91a9d15544ebc71d27c8a9a6f930f3c32ecaa4fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803684"
---
# <a name="proptype"></a><span data-ttu-id="0bf8f-103">PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="0bf8f-103">PROP_TYPE</span></span>

  
  
<span data-ttu-id="0bf8f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0bf8f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0bf8f-105">指定されたプロパティ タグのプロパティの型を返します。</span><span class="sxs-lookup"><span data-stu-id="0bf8f-105">Returns the property type of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bf8f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0bf8f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0bf8f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0bf8f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="0bf8f-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="0bf8f-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="0bf8f-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0bf8f-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_TYPE (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="0bf8f-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0bf8f-110">Parameters</span></span>

 <span data-ttu-id="0bf8f-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="0bf8f-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="0bf8f-112">プロパティ タグを取得するプロパティの型が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0bf8f-112">Property tag that contains the property type to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0bf8f-113">注釈</span><span class="sxs-lookup"><span data-stu-id="0bf8f-113">Remarks</span></span>

<span data-ttu-id="0bf8f-114">プロパティの種類を調べるには、 **PROP_TYPE**マクロを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0bf8f-114">The **PROP_TYPE** macro can be used to determine the type of a property.</span></span> <span data-ttu-id="0bf8f-115">PT_BINARY が返される値の PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) の結果を呼び出すなどです。</span><span class="sxs-lookup"><span data-stu-id="0bf8f-115">For example, calling PROP_TYPE (**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))) results in the value PT_BINARY being returned.</span></span>
  
<span data-ttu-id="0bf8f-116">プロパティのすべてのタグには、下位ワード (ビット 0 ~ 15) のプロパティの型と、上位ワード (16 ~ 31 のビット) のプロパティの識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="0bf8f-116">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="0bf8f-117">**PROP_TYPE**マクロは、プロパティの型を抽出し返される整数の 15 からビット 0 に配置します。</span><span class="sxs-lookup"><span data-stu-id="0bf8f-117">The **PROP_TYPE** macro extracts the property type and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="0bf8f-118">戻り値の残りのビットは、0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0bf8f-118">The remaining bits of the return value are set to zeros.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0bf8f-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="0bf8f-119">See also</span></span>



[<span data-ttu-id="0bf8f-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="0bf8f-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="0bf8f-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="0bf8f-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

