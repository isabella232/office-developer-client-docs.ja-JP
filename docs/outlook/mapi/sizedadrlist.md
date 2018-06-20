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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 13dad61176a877295069317e4a5b51888b01bebb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803907"
---
# <a name="sizedadrlist"></a><span data-ttu-id="fe494-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="fe494-103">SizedADRLIST</span></span>

<span data-ttu-id="fe494-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe494-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe494-105">[ADRENTRY](adrentry.md)構造体の指定した数が含まれている指定した名前の[ADRLIST](adrlist.md)構造体を定義します。</span><span class="sxs-lookup"><span data-stu-id="fe494-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fe494-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fe494-106">Header file:</span></span>  <br/> |<span data-ttu-id="fe494-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe494-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fe494-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="fe494-108">Related structure:</span></span>  <br/> |<span data-ttu-id="fe494-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="fe494-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="fe494-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="fe494-110">Parameters</span></span>

<span data-ttu-id="fe494-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="fe494-111">__centries_</span></span>
  
> <span data-ttu-id="fe494-112">新しい**ADRLIST**構造体に含まれる**ADRENTRY**構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="fe494-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="fe494-113">__名_</span><span class="sxs-lookup"><span data-stu-id="fe494-113">__name_</span></span>
  
> <span data-ttu-id="fe494-114">新しい**ADRLIST**構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="fe494-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="fe494-115">備考</span><span class="sxs-lookup"><span data-stu-id="fe494-115">Remarks</span></span>

<span data-ttu-id="fe494-116">**SizedADRLIST**マクロを使用して、配列の長さの要件がわかっている場合は、明示的な境界を持つ受信者の一覧を定義できます。</span><span class="sxs-lookup"><span data-stu-id="fe494-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="fe494-117">次のコードは、 **SizedADRLIST**マクロ、 **ADRLIST**構造体のポインターにキャストする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fe494-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="fe494-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe494-118">See also</span></span>

- [<span data-ttu-id="fe494-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="fe494-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="fe494-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="fe494-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="fe494-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="fe494-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

