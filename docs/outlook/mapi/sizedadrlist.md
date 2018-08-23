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
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574742"
---
# <a name="sizedadrlist"></a><span data-ttu-id="2b07e-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="2b07e-103">SizedADRLIST</span></span>

<span data-ttu-id="2b07e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2b07e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2b07e-105">[ADRENTRY](adrentry.md)構造体の指定した数が含まれている指定した名前の[ADRLIST](adrlist.md)構造体を定義します。</span><span class="sxs-lookup"><span data-stu-id="2b07e-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b07e-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2b07e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2b07e-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2b07e-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2b07e-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="2b07e-108">Related structure:</span></span>  <br/> |<span data-ttu-id="2b07e-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="2b07e-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="2b07e-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2b07e-110">Parameters</span></span>

<span data-ttu-id="2b07e-111">__centries_</span><span class="sxs-lookup"><span data-stu-id="2b07e-111">__centries_</span></span>
  
> <span data-ttu-id="2b07e-112">新しい**ADRLIST**構造体に含まれる**ADRENTRY**構造体の数です。</span><span class="sxs-lookup"><span data-stu-id="2b07e-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="2b07e-113">__名_</span><span class="sxs-lookup"><span data-stu-id="2b07e-113">__name_</span></span>
  
> <span data-ttu-id="2b07e-114">新しい**ADRLIST**構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="2b07e-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2b07e-115">注釈</span><span class="sxs-lookup"><span data-stu-id="2b07e-115">Remarks</span></span>

<span data-ttu-id="2b07e-116">**SizedADRLIST**マクロを使用して、配列の長さの要件がわかっている場合は、明示的な境界を持つ受信者の一覧を定義できます。</span><span class="sxs-lookup"><span data-stu-id="2b07e-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="2b07e-117">次のコードは、 **SizedADRLIST**マクロ、 **ADRLIST**構造体のポインターにキャストする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2b07e-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="2b07e-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="2b07e-118">See also</span></span>

- [<span data-ttu-id="2b07e-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="2b07e-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="2b07e-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="2b07e-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="2b07e-121">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="2b07e-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

