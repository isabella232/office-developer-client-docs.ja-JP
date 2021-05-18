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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 885cf53de45cfde4079cc2a0e7bfdca09f72b962
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404317"
---
# <a name="cbnewadrlist"></a><span data-ttu-id="38575-103">CbNewADRLIST</span><span class="sxs-lookup"><span data-stu-id="38575-103">CbNewADRLIST</span></span>

  
  
<span data-ttu-id="38575-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38575-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38575-105">[ADRENTRY](adrentry.md)構造体で表される受信者の指定した数を含む新しい[ADRLIST](adrlist.md)構造体に割り当てる必要があるバイト数を計算します。</span><span class="sxs-lookup"><span data-stu-id="38575-105">Computes the number of bytes that should be allocated for a new [ADRLIST](adrlist.md) structure that contains a specified number of recipients represented by [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38575-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="38575-106">Header file:</span></span>  <br/> |<span data-ttu-id="38575-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="38575-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="38575-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="38575-108">Related structure:</span></span>  <br/> |<span data-ttu-id="38575-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="38575-109">**ADRLIST**</span></span> <br/> |
   
```cpp
CbNewADRLIST (_centries)
```

## <a name="parameters"></a><span data-ttu-id="38575-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="38575-110">Parameters</span></span>

 <span data-ttu-id="38575-111">_ _centries_</span><span class="sxs-lookup"><span data-stu-id="38575-111">_ _centries_</span></span>
  
> <span data-ttu-id="38575-112">新しい **ADRLIST** 構造に含める **ADRENTRY** 構造体の数。</span><span class="sxs-lookup"><span data-stu-id="38575-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="38575-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="38575-113">See also</span></span>



[<span data-ttu-id="38575-114">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="38575-114">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="38575-115">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="38575-115">ADRENTRY</span></span>](adrentry.md)


[<span data-ttu-id="38575-116">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="38575-116">Macros Related to Structures</span></span>](macros-related-to-structures.md)

