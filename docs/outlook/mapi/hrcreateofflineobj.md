---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0a34c441a473154a43a107b4236ccc259d327dba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348056"
---
# <a name="hrcreateofflineobj"></a><span data-ttu-id="76602-103">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="76602-103">HrCreateOfflineObj</span></span>

<span data-ttu-id="76602-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76602-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="76602-105">オブジェクトがオンラインおよびオフラインになったときに mapi に通知するために、プロバイダーとストアによって使用される mapi オフラインオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="76602-105">Creates a MAPI offline object that is used by the provider and store in order to notify MAPI when the object goes online and offline,</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="76602-106">エクスポート対象:</span><span class="sxs-lookup"><span data-stu-id="76602-106">Exported by:</span></span>  <br/> |<span data-ttu-id="76602-107">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="76602-107">Msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="76602-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="76602-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="76602-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="76602-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="76602-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="76602-110">Called by:</span></span>  <br/> |<span data-ttu-id="76602-111">クライアント</span><span class="sxs-lookup"><span data-stu-id="76602-111">Client</span></span>  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a><span data-ttu-id="76602-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76602-112">Parameters</span></span>

<span data-ttu-id="76602-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="76602-113">_ulFlags_</span></span>
  
> <span data-ttu-id="76602-114">順番0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="76602-114">[in] It must be 0.</span></span>
    
<span data-ttu-id="76602-115">_pcreateinfo_</span><span class="sxs-lookup"><span data-stu-id="76602-115">_pCreateInfo_</span></span>
  
> <span data-ttu-id="76602-116">順番オフラインオブジェクトの作成に必要な情報が含まれている**MAPIOFFLINE_CREATEINFO**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="76602-116">[in] A pointer to a **MAPIOFFLINE_CREATEINFO** structure that contains the information needed to create the offline object.</span></span> 
    
<span data-ttu-id="76602-117">_ppoffline_</span><span class="sxs-lookup"><span data-stu-id="76602-117">_ppOffline_</span></span>
  
> <span data-ttu-id="76602-118">読み上げ**IMAPIOfflineMgr**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="76602-118">[out] A pointer to the **IMAPIOfflineMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="76602-119">Return value</span><span class="sxs-lookup"><span data-stu-id="76602-119">Return value</span></span>

<span data-ttu-id="76602-120">なし。</span><span class="sxs-lookup"><span data-stu-id="76602-120">None.</span></span>
  
<span data-ttu-id="76602-121">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="76602-121">HrOpenOfflineObj</span></span>
  
## <a name="example"></a><span data-ttu-id="76602-122">例</span><span class="sxs-lookup"><span data-stu-id="76602-122">Example</span></span>

```cpp
// create/get global offline object to use as parent.
 ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = &GUID_GlobalState;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = NULL;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
// Create an offline object for the provider with global as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = pGuid;
  OfflineCreateInfo.pInstance = pInstance;
  OfflineCreateInfo.pParent = pGlobalOfflineMgr;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
  // create store offline object which aggregates with the store object and has provider offline object as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = NULL;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = m_pProviderOfflineMgr;
  OfflineCreateInfo.pMAPISupport = pMAPISup;
  OfflineCreateInfo.pAggregateInfo = &AggregateInfo;
  OfflineCreateInfo.pConnectInfo = NULL;
  ZeroMemory(&AggregateInfo, sizeof(AggregateInfo));
  AggregateInfo.ulSize = sizeof(AggregateInfo);
  AggregateInfo.pOuterObj = (IMsgStore *)this;
  AggregateInfo.pRefTrackRoot = NULL;

```

## <a name="see-also"></a><span data-ttu-id="76602-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="76602-123">See also</span></span>

- [<span data-ttu-id="76602-124">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="76602-124">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)
- [<span data-ttu-id="76602-125">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="76602-125">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

