---
title: CbNewMTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CbNewMTSID
api_type:
- COM
ms.assetid: fd5ef226-39e6-4604-a751-2f6cc49c4895
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8ffff7958ab405e488ac2ce45bae43b78da7b0f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331599"
---
# <a name="cbnewmtsid"></a><span data-ttu-id="d889f-103">CbNewMTSID</span><span class="sxs-lookup"><span data-stu-id="d889f-103">CbNewMTSID</span></span>

  
  
<span data-ttu-id="d889f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d889f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d889f-105">指定したサイズのメッセージ転送エージェント識別子を使用して、新しい[MTSID](mtsid.md)構造に割り当てる必要があるバイト数を計算します。</span><span class="sxs-lookup"><span data-stu-id="d889f-105">Computes the number of bytes that should be allocated for a new [MTSID](mtsid.md) structure with a message transfer agent identifier of a specified size.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d889f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d889f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d889f-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d889f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="d889f-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="d889f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="d889f-109">**MTSID**</span><span class="sxs-lookup"><span data-stu-id="d889f-109">**MTSID**</span></span> <br/> |
   
```cpp
CbNewMTSID (_cb)
```

## <a name="parameters"></a><span data-ttu-id="d889f-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d889f-110">Parameters</span></span>

 <span data-ttu-id="d889f-111">__cb_</span><span class="sxs-lookup"><span data-stu-id="d889f-111">__cb_</span></span>
  
> <span data-ttu-id="d889f-112">新しい**MTSID**構造に含めるメッセージ転送エージェント識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="d889f-112">Count of bytes for the message transfer agent identifier to be included in the new **MTSID** structure.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="d889f-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="d889f-113">See also</span></span>



[<span data-ttu-id="d889f-114">MTSID</span><span class="sxs-lookup"><span data-stu-id="d889f-114">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="d889f-115">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="d889f-115">Macros Related to Structures</span></span>](macros-related-to-structures.md)

