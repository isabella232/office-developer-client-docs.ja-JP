---
title: CHANGE_PROP_TYPE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CHANGE_PROP_TYPE
api_type:
- COM
ms.assetid: 95513b5a-fd3b-46f2-a6c0-094500ae4ca7
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ee1b84e36ef014fab87ca910115675c905f6a09
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408622"
---
# <a name="change_prop_type"></a><span data-ttu-id="8e4cc-103">CHANGE_PROP_TYPE</span><span class="sxs-lookup"><span data-stu-id="8e4cc-103">CHANGE_PROP_TYPE</span></span>

  
  
<span data-ttu-id="8e4cc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e4cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e4cc-105">プロパティ タグのプロパティの種類を指定した値に更新します。</span><span class="sxs-lookup"><span data-stu-id="8e4cc-105">Updates the property type of a property tag to a specified value.</span></span> <span data-ttu-id="8e4cc-106">プロパティ識別子は変更されません。</span><span class="sxs-lookup"><span data-stu-id="8e4cc-106">The property identifier is unchanged.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8e4cc-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8e4cc-107">Header file:</span></span>  <br/> |<span data-ttu-id="8e4cc-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8e4cc-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8e4cc-109">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="8e4cc-109">Related structure:</span></span>  <br/> |[<span data-ttu-id="8e4cc-110">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8e4cc-110">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
CHANGE_PROP_TYPE (ulPropTag, ulPropType)
```

## <a name="parameters"></a><span data-ttu-id="8e4cc-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8e4cc-111">Parameters</span></span>

 <span data-ttu-id="8e4cc-112">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="8e4cc-112">_ulPropTag_</span></span>
  
> <span data-ttu-id="8e4cc-113">変更するプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="8e4cc-113">The property tag to be modified.</span></span>
    
 <span data-ttu-id="8e4cc-114">_ulPropType_</span><span class="sxs-lookup"><span data-stu-id="8e4cc-114">_ulPropType_</span></span>
  
> <span data-ttu-id="8e4cc-115">プロパティの種類の新しい値。</span><span class="sxs-lookup"><span data-stu-id="8e4cc-115">The new value for the property type.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8e4cc-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="8e4cc-116">See also</span></span>



[<span data-ttu-id="8e4cc-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="8e4cc-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="8e4cc-118">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="8e4cc-118">Macros Related to Structures</span></span>](macros-related-to-structures.md)

