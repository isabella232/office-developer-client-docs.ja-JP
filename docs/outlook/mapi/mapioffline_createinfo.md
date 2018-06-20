---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 17ab26c62bcbb57ff8e53b5412ca27ed414fb725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801511"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="4bc5f-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="4bc5f-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="4bc5f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4bc5f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4bc5f-105">この構造体は、 [HrCreateOfflineObj](hrcreateofflineobj.md)で使用されます。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="4bc5f-106">メンバー</span><span class="sxs-lookup"><span data-stu-id="4bc5f-106">Members</span></span>

 <span data-ttu-id="4bc5f-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-107">**ulSize**</span></span>
  
> <span data-ttu-id="4bc5f-108">構造体のサイズです。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-108">The size of structure.</span></span>
    
 <span data-ttu-id="4bc5f-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="4bc5f-110">0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-110">It must be 0.</span></span>
    
 <span data-ttu-id="4bc5f-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="4bc5f-112">プロファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-112">The name of the profile.</span></span>
    
 <span data-ttu-id="4bc5f-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="4bc5f-114">以下の機能フラグのビット マスクです。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="4bc5f-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="4bc5f-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="4bc5f-116">オフライン オブジェクトはオフラインになることができます。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="4bc5f-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="4bc5f-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="4bc5f-118">オフラインのオブジェクトでは、オンラインのことができます。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="4bc5f-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-119">**pGUID**</span></span>
  
> <span data-ttu-id="4bc5f-120">この種類の他のオフラインのオブジェクトからオフラインのオブジェクトを一意に識別するために使用する GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="4bc5f-121">GUID_GlobalState は、親オブジェクトとしてオブジェクトを使用するグローバル オブジェクトを参照します。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="4bc5f-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-122">**pInstance**</span></span>
  
> <span data-ttu-id="4bc5f-123">このオフラインのオブジェクトを一意に識別する GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="4bc5f-124">このオフラインの他のオブジェクトからオブジェクトを明確に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="4bc5f-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-125">**pParent**</span></span>
  
> <span data-ttu-id="4bc5f-126">オフライン オブジェクトと元の親であるオフラインのオブジェクトへのポインターはこのオフラインのオブジェクトの継承を変更します。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="4bc5f-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="4bc5f-128">MAPI サポート オブジェクトがこのオブジェクトを使用することを識別します。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="4bc5f-129">などのオフライン オブジェクトはオフラインで使用ストアの変更を追跡すると、オンラインの状態にし、これは、ストアは、オブジェクトをサポートします。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="4bc5f-130">ただし、サポート オブジェクトを持たないオブジェクトのオフライン オブジェクトは、この場合、その NULL でもかまいません。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="4bc5f-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="4bc5f-132">MAPIOFFLINE_AGGREGATEINFO 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="4bc5f-133">詳細については、 [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="4bc5f-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="4bc5f-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="4bc5f-135">Null にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4bc5f-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4bc5f-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="4bc5f-136">See also</span></span>



[<span data-ttu-id="4bc5f-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="4bc5f-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="4bc5f-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="4bc5f-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

