---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566664"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="ca6f6-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="ca6f6-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="ca6f6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca6f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca6f6-105">同じ識別子が含まれているかどうかを決定する 2 つの[MAPIUID](mapiuid.md)構造体をテストします。</span><span class="sxs-lookup"><span data-stu-id="ca6f6-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ca6f6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ca6f6-106">Header file:</span></span>  <br/> |<span data-ttu-id="ca6f6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ca6f6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ca6f6-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="ca6f6-108">Related structure:</span></span>  <br/> |<span data-ttu-id="ca6f6-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="ca6f6-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="ca6f6-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ca6f6-110">Parameters</span></span>

 <span data-ttu-id="ca6f6-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="ca6f6-111">_lpuid1_</span></span>
  
> <span data-ttu-id="ca6f6-112">テストする最初の**MAPIUID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca6f6-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="ca6f6-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="ca6f6-113">_lpuid2_</span></span>
  
> <span data-ttu-id="ca6f6-114">テストする 2 番目の**MAPIUID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ca6f6-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ca6f6-115">注釈</span><span class="sxs-lookup"><span data-stu-id="ca6f6-115">Remarks</span></span>

<span data-ttu-id="ca6f6-116">**IsEqualMAPIUID**マクロは、2 つの**MAPIUID**構造体が含まれる場合、同じ識別子と FALSE そうでない場合に TRUE を返します。</span><span class="sxs-lookup"><span data-stu-id="ca6f6-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="ca6f6-117">**IsEqualMAPIUID**マクロには、ヘッダー ファイル Memory.h が含まれていることが必要です。</span><span class="sxs-lookup"><span data-stu-id="ca6f6-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca6f6-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="ca6f6-118">See also</span></span>



[<span data-ttu-id="ca6f6-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ca6f6-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="ca6f6-120">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="ca6f6-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

