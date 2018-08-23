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
ms.openlocfilehash: 0f1495549df751c59ab84e2b16fffbaf2f4f9fa5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574721"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="762fe-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="762fe-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="762fe-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="762fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="762fe-105">それぞれの X.400 メッセージ転送システム (MTS) エントリ識別子が含まれています、 [MTSID](mtsid.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="762fe-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="762fe-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="762fe-106">Header file:</span></span>  <br/> |<span data-ttu-id="762fe-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="762fe-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="762fe-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="762fe-108">Related macros:</span></span>  <br/> |<span data-ttu-id="762fe-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md)、 [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="762fe-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="762fe-110">Members</span><span class="sxs-lookup"><span data-stu-id="762fe-110">Members</span></span>

 <span data-ttu-id="762fe-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="762fe-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="762fe-112">**MTSID**の構造体**abMTSIDs**のメンバーによって説明されている配列内の数です。</span><span class="sxs-lookup"><span data-stu-id="762fe-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="762fe-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="762fe-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="762fe-114">**AbMTSIDs**で説明されている配列内のバイト数。</span><span class="sxs-lookup"><span data-stu-id="762fe-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="762fe-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="762fe-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="762fe-116">**MTSID**の構造体 1 つまたは複数にはが含まれているバイト配列。</span><span class="sxs-lookup"><span data-stu-id="762fe-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="762fe-117">注釈</span><span class="sxs-lookup"><span data-stu-id="762fe-117">Remarks</span></span>

<span data-ttu-id="762fe-118">X.400 メッセージングの**FLATMTSIDLIST**構造体の使用は、MAPI メッセージの[FLATENTRYLIST](flatentrylist.md)構造体の使用に対応します。</span><span class="sxs-lookup"><span data-stu-id="762fe-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="762fe-119">MAPI は、メッセージの処理中に、X.400 のプロパティを維持するために**FLATMTSIDLIST**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="762fe-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="762fe-120">サービス プロバイダーは、着信および発信 X.400 メッセージを処理する場合、 **FLATMTSIDLIST**構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="762fe-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="762fe-121">**AbMTSIDs**アレイでは、 **MTSID**の各構造体が揃えられた自然な境界に揃えられます。</span><span class="sxs-lookup"><span data-stu-id="762fe-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="762fe-122">余分なバイトは、確かに自然の配置の 2 つの**MTSID**構造体の間に埋め込み文字として含まれます。</span><span class="sxs-lookup"><span data-stu-id="762fe-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="762fe-123">配列内の最初の**MTSID**構造体は、 **abMTSIDs**メンバーのオフセットが 8 であるために常に、正しく配置されます。</span><span class="sxs-lookup"><span data-stu-id="762fe-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="762fe-124">次の構造体のオフセットの計算には、最初のエントリのサイズを使用して、次に 4 の倍数に切り上げられます。</span><span class="sxs-lookup"><span data-stu-id="762fe-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="762fe-125">**MTSID**構造体のサイズを計算するのにには、 [CbNewMTSID](cbnewmtsid.md)マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="762fe-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="762fe-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="762fe-126">See also</span></span>



[<span data-ttu-id="762fe-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="762fe-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="762fe-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="762fe-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="762fe-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="762fe-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="762fe-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="762fe-130">MAPI Structures</span></span>](mapi-structures.md)

