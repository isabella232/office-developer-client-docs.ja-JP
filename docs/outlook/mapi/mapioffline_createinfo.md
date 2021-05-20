---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429566"
---
# <a name="mapioffline_createinfo"></a><span data-ttu-id="e2dcf-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="e2dcf-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="e2dcf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2dcf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2dcf-105">この構造は [、HrCreateOfflineObj で使用されます](hrcreateofflineobj.md)。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a><span data-ttu-id="e2dcf-106">Members</span><span class="sxs-lookup"><span data-stu-id="e2dcf-106">Members</span></span>

 <span data-ttu-id="e2dcf-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-107">**ulSize**</span></span>
  
> <span data-ttu-id="e2dcf-108">構造体のサイズ。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-108">The size of structure.</span></span>
    
 <span data-ttu-id="e2dcf-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="e2dcf-110">0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-110">It must be 0.</span></span>
    
 <span data-ttu-id="e2dcf-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="e2dcf-112">プロファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-112">The name of the profile.</span></span>
    
 <span data-ttu-id="e2dcf-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="e2dcf-114">次の機能フラグのビット マスク。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="e2dcf-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="e2dcf-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="e2dcf-116">オフライン オブジェクトはオフラインにできます。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="e2dcf-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="e2dcf-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="e2dcf-118">オフライン オブジェクトはオンラインにできます。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="e2dcf-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-119">**pGUID**</span></span>
  
> <span data-ttu-id="e2dcf-120">他のオフライン オブジェクトからこの種類のオフライン オブジェクトを一意に識別するために使用される GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="e2dcf-121">GUID_GlobalStateは、オブジェクトが親オブジェクトとして使用できるグローバル オフライン オブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="e2dcf-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-122">**pInstance**</span></span>
  
> <span data-ttu-id="e2dcf-123">このオフライン オブジェクトを一意に識別する GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="e2dcf-124">このオフライン オブジェクトを他のオブジェクトからあいまいに解除するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="e2dcf-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-125">**pParent**</span></span>
  
> <span data-ttu-id="e2dcf-126">このオフライン オブジェクトの親であり、このオフライン オブジェクトが継承する変更を持つオフライン オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="e2dcf-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="e2dcf-128">このオフライン オブジェクトを使用する MAPI サポート オブジェクトを識別します。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="e2dcf-129">たとえば、このオフライン オブジェクトを使用してストアのオフライン状態とオンライン状態を追跡する場合、これが stores サポート オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="e2dcf-130">ただし、サポート オブジェクトがないオブジェクトのオフライン オブジェクトの場合は、NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="e2dcf-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="e2dcf-132">構造体へのポインター MAPIOFFLINE_AGGREGATEINFOします。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="e2dcf-133">詳細については、「MAPIOFFLINE_AGGREGATEINFO」 [を参照してください](mapioffline_aggregateinfo.md)。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="e2dcf-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="e2dcf-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="e2dcf-135">null である必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2dcf-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e2dcf-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2dcf-136">See also</span></span>



[<span data-ttu-id="e2dcf-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="e2dcf-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="e2dcf-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="e2dcf-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

