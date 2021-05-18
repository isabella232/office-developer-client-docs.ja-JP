---
title: PROP_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PROP_ID
api_type:
- COM
ms.assetid: 6ddaced5-49bb-41fe-95da-4e3300883bf7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 228ea91969b35a1608dd6b3378b751312aa9c665
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409133"
---
# <a name="prop_id"></a><span data-ttu-id="76334-103">PROP_ID</span><span class="sxs-lookup"><span data-stu-id="76334-103">PROP_ID</span></span>

  
  
<span data-ttu-id="76334-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76334-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76334-105">指定したプロパティ タグのプロパティ識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="76334-105">Returns the property identifier of a specified property tag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76334-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="76334-106">Header file:</span></span>  <br/> |<span data-ttu-id="76334-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="76334-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="76334-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="76334-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="76334-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="76334-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
PROP_ID (ulPropTag)
```

## <a name="parameters"></a><span data-ttu-id="76334-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76334-110">Parameters</span></span>

 <span data-ttu-id="76334-111">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="76334-111">_ulPropTag_</span></span>
  
> <span data-ttu-id="76334-112">返される識別子を含むプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="76334-112">Property tag that contains the identifier to be returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="76334-113">注釈</span><span class="sxs-lookup"><span data-stu-id="76334-113">Remarks</span></span>

<span data-ttu-id="76334-114">すべてのプロパティ タグには、低次ワード (ビット 0 ~ 15) のプロパティ型と、高次ワード (ビット 16 ~ 31) のプロパティ識別子が含まれる。</span><span class="sxs-lookup"><span data-stu-id="76334-114">Every property tag contains the property type in the low-order word (bits 0 through 15) and the property identifier in the high-order word (bits 16 through 31).</span></span> <span data-ttu-id="76334-115">この **PROP_ID** は、プロパティ識別子を抽出し、返される整数のビット 0 ~ 15 に格納します。</span><span class="sxs-lookup"><span data-stu-id="76334-115">The **PROP_ID** macro extracts the property identifier and puts it in bits 0 through 15 of the integer to be returned.</span></span> <span data-ttu-id="76334-116">戻り値の残りのビットは 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="76334-116">The remaining bits of the return value are set to zeros.</span></span> 
  
<span data-ttu-id="76334-117">たとえば **PROP_ID** マクロを使用して [、IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)に渡す識別子を取得できます。</span><span class="sxs-lookup"><span data-stu-id="76334-117">The **PROP_ID** macro can be used, for example, to retrieve an identifier to pass to [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> <span data-ttu-id="76334-118">**GetNamesFromIDs は** 、名前付きプロパティの識別子に関連付けられたプロパティ名を取得します。</span><span class="sxs-lookup"><span data-stu-id="76334-118">**GetNamesFromIDs** retrieves the property name associated with an identifier for a named property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76334-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="76334-119">See also</span></span>



[<span data-ttu-id="76334-120">SPropValue</span><span class="sxs-lookup"><span data-stu-id="76334-120">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="76334-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="76334-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

