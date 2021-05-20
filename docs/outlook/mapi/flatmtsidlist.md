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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439220"
---
# <a name="flatmtsidlist"></a><span data-ttu-id="036d3-103">FLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="036d3-103">FLATMTSIDLIST</span></span>

  
  
<span data-ttu-id="036d3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="036d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="036d3-105">[MTSID 構造体の配列を含](mtsid.md)み、それぞれ X.400 メッセージ トランスポート システム (MTS) エントリ識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="036d3-105">Contains an array of [MTSID](mtsid.md) structures, each of which contains an X.400 message transport system (MTS) entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="036d3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="036d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="036d3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="036d3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="036d3-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="036d3-108">Related macros:</span></span>  <br/> |<span data-ttu-id="036d3-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md)、 [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span><span class="sxs-lookup"><span data-stu-id="036d3-109">[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)</span></span> <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a><span data-ttu-id="036d3-110">Members</span><span class="sxs-lookup"><span data-stu-id="036d3-110">Members</span></span>

 <span data-ttu-id="036d3-111">**cMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="036d3-111">**cMTSIDs**</span></span>
  
> <span data-ttu-id="036d3-112">**abMTSIDs** メンバーによって記述された配列内の **MTSID** 構造体の数。</span><span class="sxs-lookup"><span data-stu-id="036d3-112">Count of **MTSID** structures in the array described by the **abMTSIDs** member.</span></span> 
    
 <span data-ttu-id="036d3-113">**cbMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="036d3-113">**cbMTSIDs**</span></span>
  
> <span data-ttu-id="036d3-114">**abMTSIDs** で記述された配列内のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="036d3-114">Count of bytes in the array described by **abMTSIDs**.</span></span>
    
 <span data-ttu-id="036d3-115">**abMTSIDs**</span><span class="sxs-lookup"><span data-stu-id="036d3-115">**abMTSIDs**</span></span>
  
> <span data-ttu-id="036d3-116">1 つ以上の **MTSID 構造体を含むバイト** 配列。</span><span class="sxs-lookup"><span data-stu-id="036d3-116">Byte array that contains one or more **MTSID** structures.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="036d3-117">注釈</span><span class="sxs-lookup"><span data-stu-id="036d3-117">Remarks</span></span>

<span data-ttu-id="036d3-118">X.400 メッセージングでの **FLATMTSIDLIST** 構造体の使用は、MAPI メッセージングでの [FLATENTRYLIST](flatentrylist.md) 構造体の使用に対応します。</span><span class="sxs-lookup"><span data-stu-id="036d3-118">The **FLATMTSIDLIST** structure's use in X.400 messaging corresponds to the [FLATENTRYLIST](flatentrylist.md) structure's use in MAPI messaging.</span></span> <span data-ttu-id="036d3-119">MAPI では **、FLATMTSIDLIST** 構造体を使用して、メッセージの処理中に X.400 プロパティを維持します。</span><span class="sxs-lookup"><span data-stu-id="036d3-119">MAPI uses **FLATMTSIDLIST** structures to maintain X.400 properties during message handling.</span></span> <span data-ttu-id="036d3-120">サービス プロバイダーは、受信メッセージと送信 X.400 メッセージを処理するときに **FLATMTSIDLIST** 構造体を使用します。</span><span class="sxs-lookup"><span data-stu-id="036d3-120">Service providers use **FLATMTSIDLIST** structures when handling incoming and outgoing X.400 messages.</span></span> 
  
<span data-ttu-id="036d3-121">**abMTSIDs 配列では**、**各 MTSID** 構造体は自然に整列された境界に配置されます。</span><span class="sxs-lookup"><span data-stu-id="036d3-121">In the **abMTSIDs** array, each **MTSID** structure is aligned on a naturally aligned boundary.</span></span> <span data-ttu-id="036d3-122">余分なバイトは、任意の 2 つの MTSID 構造体間の自然な配置を確認するために埋め **込みとして含** まれます。</span><span class="sxs-lookup"><span data-stu-id="036d3-122">Extra bytes are included as padding to make sure natural alignment between any two **MTSID** structures.</span></span> <span data-ttu-id="036d3-123">配列内 **の最初の MTSID** 構造体は **、abMTSIDs** メンバーのオフセットが 8 なので、常に正しく配置されます。</span><span class="sxs-lookup"><span data-stu-id="036d3-123">The first **MTSID** structure in the array is always aligned correctly because the offset of the **abMTSIDs** member is 8.</span></span> <span data-ttu-id="036d3-124">次の構造体のオフセットを計算するには、4 の次の倍数に切り上げ、最初のエントリのサイズを使用します。</span><span class="sxs-lookup"><span data-stu-id="036d3-124">To compute the offset of the next structure, use the size of the first entry rounded up to the next multiple of 4.</span></span> <span data-ttu-id="036d3-125">[CbNewMTSID マクロを使用](cbnewmtsid.md)して **、MTSID** 構造のサイズを計算します。</span><span class="sxs-lookup"><span data-stu-id="036d3-125">Use the [CbNewMTSID](cbnewmtsid.md) macro to compute the size of an **MTSID** structure.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="036d3-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="036d3-126">See also</span></span>



[<span data-ttu-id="036d3-127">CbNewFLATMTSIDLIST</span><span class="sxs-lookup"><span data-stu-id="036d3-127">CbNewFLATMTSIDLIST</span></span>](cbnewflatmtsidlist.md)
  
[<span data-ttu-id="036d3-128">FLATENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="036d3-128">FLATENTRYLIST</span></span>](flatentrylist.md)
  
[<span data-ttu-id="036d3-129">MTSID</span><span class="sxs-lookup"><span data-stu-id="036d3-129">MTSID</span></span>](mtsid.md)


[<span data-ttu-id="036d3-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="036d3-130">MAPI Structures</span></span>](mapi-structures.md)

