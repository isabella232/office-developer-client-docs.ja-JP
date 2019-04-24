---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327308"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="ae1d5-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="ae1d5-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="ae1d5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae1d5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae1d5-105">には、 [MTSID](mtsid.md)構造体の配列が格納されています。それぞれには、1つのメッセージトランスポートシステム (MTS) エントリ識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae1d5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ae1d5-106">Header file:</span></span>  <br/> |<span data-ttu-id="ae1d5-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae1d5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ae1d5-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="ae1d5-108">Related macros:</span></span>  <br/> |<span data-ttu-id="ae1d5-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md)、 [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="ae1d5-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="ae1d5-110">Members</span><span class="sxs-lookup"><span data-stu-id="ae1d5-110">Members</span></span>

 <span data-ttu-id="ae1d5-111">**cmtsids**</span><span class="sxs-lookup"><span data-stu-id="ae1d5-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="ae1d5-112">**abmtsids**メンバーによって記述された、配列内の**MTSID**構造体の数。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="ae1d5-113">**cbmtsids**</span><span class="sxs-lookup"><span data-stu-id="ae1d5-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="ae1d5-114">**abmtsids**で記述された配列のバイト数。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="ae1d5-115">**abmtsids**</span><span class="sxs-lookup"><span data-stu-id="ae1d5-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="ae1d5-116">1つまたは複数の**MTSID**構造体を含むバイト配列。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ae1d5-117">解説</span><span class="sxs-lookup"><span data-stu-id="ae1d5-117">Remarks</span></span>

<span data-ttu-id="ae1d5-118">**FLATMTSIDLIST**におけるこの構造体の使用は、MAPI メッセージングでの[FLATENTRYLIST](flatentrylist.md)構造の使用に対応しています。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="ae1d5-119">MAPI では、 **FLATMTSIDLIST**構造を使用して、メッセージ処理時に x. プロパティを維持します。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="ae1d5-120">サービスプロバイダーは、受信および送信の X. 400 メッセージを処理するときに、 **FLATMTSIDLIST**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="ae1d5-121">**abmtsids**配列では、各**MTSID**構造は、自然に配置された境界に沿って配置されます。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="ae1d5-122">2つの**MTSID**構造体間で自然な配置が行われるように、パディングとして追加のバイトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="ae1d5-123">**abmtsids**メンバのオフセットは8であるため、配列内の最初の**MTSID**構造体は常に正確に調整されます。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="ae1d5-124">次の構造体のオフセットを計算するには、最初のエントリのサイズを、次の4つの倍数まで切り上げて使用します。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="ae1d5-125">[CbNewMTSID](cbnewmtsid.md)マクロを使用して、 **MTSID**構造体のサイズを計算します。</span><span class="sxs-lookup"><span data-stu-id="ae1d5-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae1d5-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae1d5-126">See also</span></span>



[<span data-ttu-id="ae1d5-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="ae1d5-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="ae1d5-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="ae1d5-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="ae1d5-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="ae1d5-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="ae1d5-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ae1d5-130">MAPI Structures</span></span>](mapi-structures.md)

