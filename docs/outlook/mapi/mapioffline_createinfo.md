---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357128"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="da69f-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="da69f-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="da69f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da69f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da69f-105">この構造体は、 [hrcreateofflineobj](hrcreateofflineobj.md)と組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="da69f-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="da69f-106">Members</span><span class="sxs-lookup"><span data-stu-id="da69f-106">Members</span></span>

 <span data-ttu-id="da69f-107">**ulsize**</span><span class="sxs-lookup"><span data-stu-id="da69f-107">**ulSize**</span></span>
  
> <span data-ttu-id="da69f-108">構造体のサイズ。</span><span class="sxs-lookup"><span data-stu-id="da69f-108">The size of structure.</span></span>
    
 <span data-ttu-id="da69f-109">**ulcreateflags**</span><span class="sxs-lookup"><span data-stu-id="da69f-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="da69f-110">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="da69f-110">It must be 0.</span></span>
    
 <span data-ttu-id="da69f-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="da69f-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="da69f-112">プロファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="da69f-112">The name of the profile.</span></span>
    
 <span data-ttu-id="da69f-113">**ulcapabilities**</span><span class="sxs-lookup"><span data-stu-id="da69f-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="da69f-114">次の機能フラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="da69f-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="da69f-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="da69f-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="da69f-116">オフラインオブジェクトがオフラインになることができる。</span><span class="sxs-lookup"><span data-stu-id="da69f-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="da69f-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="da69f-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="da69f-118">オフラインオブジェクトがオンラインになることができる。</span><span class="sxs-lookup"><span data-stu-id="da69f-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="da69f-119">**pguid**</span><span class="sxs-lookup"><span data-stu-id="da69f-119">**pGUID**</span></span>
  
> <span data-ttu-id="da69f-120">他のオフラインオブジェクトからこの種類のオフラインオブジェクトを一意に識別するために使用される GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="da69f-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="da69f-121">GUID_GlobalState は、オブジェクトが親オブジェクトとして使用できるグローバルオフラインオブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="da69f-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="da69f-122">**pinstance**</span><span class="sxs-lookup"><span data-stu-id="da69f-122">**pInstance**</span></span>
  
> <span data-ttu-id="da69f-123">このオフラインオブジェクトを一意に識別する GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="da69f-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="da69f-124">これは、このオフラインオブジェクトを他のオブジェクトからあいまいにするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="da69f-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="da69f-125">**pparent**</span><span class="sxs-lookup"><span data-stu-id="da69f-125">**pParent**</span></span>
  
> <span data-ttu-id="da69f-126">このオフラインオブジェクトの親であるオフラインオブジェクトへのポインター。このオフラインオブジェクトの変更内容が継承されます。</span><span class="sxs-lookup"><span data-stu-id="da69f-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="da69f-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="da69f-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="da69f-128">このオフラインオブジェクトを使用する MAPI サポートオブジェクトを識別します。</span><span class="sxs-lookup"><span data-stu-id="da69f-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="da69f-129">たとえば、このオフラインオブジェクトを使用してストアのオフラインとオンラインの状態を追跡している場合は、ストアのサポートオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="da69f-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="da69f-130">ただし、これがサポートオブジェクトのないオブジェクトのオフラインオブジェクトである場合は、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="da69f-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="da69f-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="da69f-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="da69f-132">MAPIOFFLINE_AGGREGATEINFO 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="da69f-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="da69f-133">詳細については、「 [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da69f-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="da69f-134">**pconnectinfo**</span><span class="sxs-lookup"><span data-stu-id="da69f-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="da69f-135">null である必要があります。</span><span class="sxs-lookup"><span data-stu-id="da69f-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da69f-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="da69f-136">See also</span></span>



[<span data-ttu-id="da69f-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="da69f-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="da69f-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="da69f-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

