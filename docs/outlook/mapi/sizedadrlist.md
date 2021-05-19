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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423462"
---
# <a name="sizedadrlist"></a><span data-ttu-id="b6429-103">SizedADRLIST</span><span class="sxs-lookup"><span data-stu-id="b6429-103">SizedADRLIST</span></span>

<span data-ttu-id="b6429-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6429-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6429-105">指定した [数の ADRENTRY](adrlist.md) 構造体を含む、指定した名前の [ADRLIST 構造体を定義](adrentry.md) します。</span><span class="sxs-lookup"><span data-stu-id="b6429-105">Defines an [ADRLIST](adrlist.md) structure with the specified name that contains a specified number of [ADRENTRY](adrentry.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6429-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b6429-106">Header file:</span></span>  <br/> |<span data-ttu-id="b6429-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b6429-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b6429-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="b6429-108">Related structure:</span></span>  <br/> |<span data-ttu-id="b6429-109">**ADRLIST**</span><span class="sxs-lookup"><span data-stu-id="b6429-109">**ADRLIST**</span></span> <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a><span data-ttu-id="b6429-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b6429-110">Parameters</span></span>

<span data-ttu-id="b6429-111">_ _centries_</span><span class="sxs-lookup"><span data-stu-id="b6429-111">_ _centries_</span></span>
  
> <span data-ttu-id="b6429-112">新しい **ADRLIST** 構造に含める **ADRENTRY** 構造体の数。</span><span class="sxs-lookup"><span data-stu-id="b6429-112">Count of **ADRENTRY** structures to be included in the new **ADRLIST** structure.</span></span> 
    
<span data-ttu-id="b6429-113">_ _name_</span><span class="sxs-lookup"><span data-stu-id="b6429-113">_ _name_</span></span>
  
> <span data-ttu-id="b6429-114">新しい **ADRLIST 構造の名前** 。</span><span class="sxs-lookup"><span data-stu-id="b6429-114">Name for the new **ADRLIST** structure.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b6429-115">注釈</span><span class="sxs-lookup"><span data-stu-id="b6429-115">Remarks</span></span>

<span data-ttu-id="b6429-116">**SizedADRLIST** マクロを使用すると、配列の長さの要件が分かっているときに明示的な境界を持つ受信者リストを定義できます。</span><span class="sxs-lookup"><span data-stu-id="b6429-116">The **SizedADRLIST** macro lets you define a recipient list that has explicit bounds when array length requirements are known.</span></span> <span data-ttu-id="b6429-117">次のコードは **、SizedADRLIST** マクロの結果を **ADRLIST 構造ポインターにキャストする方法を** 示しています。</span><span class="sxs-lookup"><span data-stu-id="b6429-117">The following code shows how to cast the result of the **SizedADRLIST** macro to an **ADRLIST** structure pointer:</span></span> 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a><span data-ttu-id="b6429-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="b6429-118">See also</span></span>

- [<span data-ttu-id="b6429-119">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="b6429-119">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="b6429-120">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="b6429-120">ADRENTRY</span></span>](adrentry.md)
- [<span data-ttu-id="b6429-121">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="b6429-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

