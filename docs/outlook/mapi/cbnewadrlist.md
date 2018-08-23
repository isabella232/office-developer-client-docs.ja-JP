---
title: CbNewADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CbNewADRLIST
api_type:
- COM
ms.assetid: 9ec1bbaa-7707-4239-9994-21ad1116430b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0bbad04e728c9283df0a9b7ceb7a8e303f0595dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799759"
---
# <a name="cbnewadrlist"></a><span data-ttu-id="992bf-103">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="992bf-103">CbNewADRLIST</span></span>

  
  
<span data-ttu-id="992bf-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="992bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="992bf-105">[ADRENTRY](adrentry.md)構造体で表される受信者の指定した番号を含む新しい[ADRLIST](adrlist.md)構造体に割り当てるバイト数を計算します。</span><span class="sxs-lookup"><span data-stu-id="992bf-105">Computes the number of bytes that should be allocated for a new [ADRLIST](adrlist.md) structure that contains a specified number of recipients represented by [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="992bf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="992bf-106">Header file:</span></span>  <br/> |<span data-ttu-id="992bf-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="992bf-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="992bf-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="992bf-108">Related structure:</span></span>  <br/> |<span data-ttu-id="992bf-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="992bf-109">**ADRLIST**</span></span> <br/> |
   
```cpp
CbNewADRLIST (_centries)
```

## <a name="parameters"></a><span data-ttu-id="992bf-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="992bf-110">Parameters</span></span>

 <span data-ttu-id="992bf-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="992bf-111">__centries_</span></span>
  
> <span data-ttu-id="992bf-112">新しい**ADRLIST**構造体に含まれる**ADRENTRY**構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="992bf-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="992bf-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="992bf-113">See also</span></span>



[<span data-ttu-id="992bf-114">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="992bf-114">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="992bf-115">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="992bf-115">ADRENTRY</span></span>](adrentry.md)


[<span data-ttu-id="992bf-116">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="992bf-116">Macros Related to Structures</span></span>](macros-related-to-structures.md)

