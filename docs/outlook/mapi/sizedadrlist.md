---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282776"
---
# <a name="sizedadrlist"></a><span data-ttu-id="5a067-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="5a067-103">SizedADRLIST</span></span>

<span data-ttu-id="5a067-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a067-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a067-105">指定された名前を持つ[adrlist](adrlist.md)構造を定義します。この構造体には、指定した数の[adrlist](adrentry.md)構造が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5a067-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5a067-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5a067-106">Header file:</span></span>  <br/> |<span data-ttu-id="5a067-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5a067-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5a067-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="5a067-108">Related structure:</span></span>  <br/> |<span data-ttu-id="5a067-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="5a067-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="5a067-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5a067-110">Parameters</span></span>

<span data-ttu-id="5a067-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="5a067-111">__centries_</span></span>
  
> <span data-ttu-id="5a067-112">新しい**adrentry**構造に含める**adrentry**構造体の数。</span><span class="sxs-lookup"><span data-stu-id="5a067-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="5a067-113">__名前_</span><span class="sxs-lookup"><span data-stu-id="5a067-113">__name_</span></span>
  
> <span data-ttu-id="5a067-114">新しい**adrlist**構造体の名前。</span><span class="sxs-lookup"><span data-stu-id="5a067-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5a067-115">解説</span><span class="sxs-lookup"><span data-stu-id="5a067-115">Remarks</span></span>

<span data-ttu-id="5a067-116">**sizedadrlist**マクロを使用すると、配列の長さの要件がわかっている場合に、明示的な境界を持つ受信者リストを定義できます。</span><span class="sxs-lookup"><span data-stu-id="5a067-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="5a067-117">次のコードは、 **sizedadrlist**マクロの結果を**adrlist**構造体のポインターにキャストする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5a067-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="5a067-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a067-118">See also</span></span>

- [<span data-ttu-id="5a067-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="5a067-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="5a067-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="5a067-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="5a067-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="5a067-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

