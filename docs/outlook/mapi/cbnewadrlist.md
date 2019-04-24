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
ms.openlocfilehash: 885cf53de45cfde4079cc2a0e7bfdca09f72b962
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329527"
---
# <a name="cbnewadrlist"></a><span data-ttu-id="2d0a2-103">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="2d0a2-103">CbNewADRLIST</span></span>

  
  
<span data-ttu-id="2d0a2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d0a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d0a2-105">[adrlist](adrentry.md)構造体で表される指定された数の受信者を含む、新しい[adrlist](adrlist.md)構造体に割り当てる必要があるバイト数を計算します。</span><span class="sxs-lookup"><span data-stu-id="2d0a2-105">Computes the number of bytes that should be allocated for a new [ADRLIST](adrlist.md) structure that contains a specified number of recipients represented by [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d0a2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2d0a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="2d0a2-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d0a2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2d0a2-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="2d0a2-108">Related structure:</span></span>  <br/> |<span data-ttu-id="2d0a2-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="2d0a2-109">**ADRLIST**</span></span> <br/> |
   
```cpp
CbNewADRLIST (_centries)
```

## <a name="parameters"></a><span data-ttu-id="2d0a2-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2d0a2-110">Parameters</span></span>

 <span data-ttu-id="2d0a2-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="2d0a2-111">__centries_</span></span>
  
> <span data-ttu-id="2d0a2-112">新しい**adrentry**構造に含める**adrentry**構造体の数。</span><span class="sxs-lookup"><span data-stu-id="2d0a2-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="2d0a2-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d0a2-113">See also</span></span>



[<span data-ttu-id="2d0a2-114">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="2d0a2-114">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="2d0a2-115">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="2d0a2-115">ADRENTRY</span></span>](adrentry.md)


[<span data-ttu-id="2d0a2-116">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="2d0a2-116">Macros Related to Structures</span></span>](macros-related-to-structures.md)

