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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426934"
---
# <a name="isequalmapiuid"></a><span data-ttu-id="f4419-103">IsEqualMAPIUID</span><span class="sxs-lookup"><span data-stu-id="f4419-103">IsEqualMAPIUID</span></span>

  
  
<span data-ttu-id="f4419-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4419-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4419-105">2つの[MAPIUID](mapiuid.md)構造体をテストして、同じ識別子を含んでいるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f4419-105">Tests two [MAPIUID](mapiuid.md) structures to determine whether they contain the same identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4419-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f4419-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4419-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f4419-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f4419-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="f4419-108">Related structure:</span></span>  <br/> |<span data-ttu-id="f4419-109">**MAPIUID**</span><span class="sxs-lookup"><span data-stu-id="f4419-109">**MAPIUID**</span></span> <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a><span data-ttu-id="f4419-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f4419-110">Parameters</span></span>

 <span data-ttu-id="f4419-111">_lpuid1_</span><span class="sxs-lookup"><span data-stu-id="f4419-111">_lpuid1_</span></span>
  
> <span data-ttu-id="f4419-112">テストする最初の**MAPIUID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f4419-112">Pointer to the first **MAPIUID** structure to be tested.</span></span> 
    
 <span data-ttu-id="f4419-113">_lpuid2_</span><span class="sxs-lookup"><span data-stu-id="f4419-113">_lpuid2_</span></span>
  
> <span data-ttu-id="f4419-114">テストする2番目の**MAPIUID**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f4419-114">Pointer to the second **MAPIUID** structure to be tested.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f4419-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f4419-115">Remarks</span></span>

<span data-ttu-id="f4419-116">**IsEqualMAPIUID**マクロは、2つの**MAPIUID**構造体に同じ識別子が含まれている場合は TRUE を返し、そうでない場合は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="f4419-116">The **IsEqualMAPIUID** macro returns TRUE if the two **MAPIUID** structures contain the same identifier and FALSE if they do not.</span></span> 
  
<span data-ttu-id="f4419-117">**IsEqualMAPIUID**マクロを使用するには、ヘッダーファイルのメモリを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4419-117">The **IsEqualMAPIUID** macro requires that the header file Memory.h be included.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4419-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="f4419-118">See also</span></span>



[<span data-ttu-id="f4419-119">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="f4419-119">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="f4419-120">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="f4419-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

