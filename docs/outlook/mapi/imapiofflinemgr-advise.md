---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3ca7fdc39da8d3ee8ecf6f0f253284df10a392e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426920"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="3d9af-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="3d9af-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="3d9af-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d9af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d9af-105">オフライン オブジェクトでコールバックを受信するクライアントを登録します。</span><span class="sxs-lookup"><span data-stu-id="3d9af-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="3d9af-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3d9af-106">Parameters</span></span>

 <span data-ttu-id="3d9af-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d9af-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="3d9af-108">[in]動作を変更するフラグ。</span><span class="sxs-lookup"><span data-stu-id="3d9af-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="3d9af-109">サポートされている値MAPIOFFLINE_ADVISE_DEFAULT指定します。</span><span class="sxs-lookup"><span data-stu-id="3d9af-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="3d9af-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="3d9af-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="3d9af-111">[in]コールバックの種類、コールバックを受信する場合、呼び出し元のコールバック インターフェイス、その他の詳細に関する情報。</span><span class="sxs-lookup"><span data-stu-id="3d9af-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="3d9af-112">また、後続の通知コールバックをクライアントの呼びOutlookに送信する場合に使用するクライアント トークンも含まれます。</span><span class="sxs-lookup"><span data-stu-id="3d9af-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="3d9af-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="3d9af-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="3d9af-114">[out]その後、オブジェクトのコールバックをキャンセルするためにクライアントの呼び出し元に返されるアドバイス トークン。</span><span class="sxs-lookup"><span data-stu-id="3d9af-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d9af-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="3d9af-115">Return value</span></span>

<span data-ttu-id="3d9af-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d9af-116">S_OK</span></span>
  
> <span data-ttu-id="3d9af-117">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="3d9af-117">The call was successful.</span></span>
    
<span data-ttu-id="3d9af-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3d9af-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="3d9af-119">無効なパラメーターが指定されています。</span><span class="sxs-lookup"><span data-stu-id="3d9af-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="3d9af-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="3d9af-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="3d9af-121">*pAdviseInfo* で指定されたコールバック インターフェイスが無効です。</span><span class="sxs-lookup"><span data-stu-id="3d9af-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3d9af-122">注釈</span><span class="sxs-lookup"><span data-stu-id="3d9af-122">Remarks</span></span>

<span data-ttu-id="3d9af-123">**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してオフライン オブジェクトを開く場合、クライアントは **IMAPIOfflineMgr** をサポートするオフライン オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="3d9af-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="3d9af-124">クライアントは **[、IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を使用して、オブジェクトでサポートされるコールバックの種類を確認できます。</span><span class="sxs-lookup"><span data-stu-id="3d9af-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="3d9af-125">クライアントは、必要なコールバックの種類と他の詳細を特定し **、IMAPIOfflineMgr::Advise** を呼び出して、オブジェクトに関するそのようなコールバックを受け取る登録を行います。</span><span class="sxs-lookup"><span data-stu-id="3d9af-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d9af-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d9af-126">See also</span></span>



[<span data-ttu-id="3d9af-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="3d9af-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="3d9af-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="3d9af-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="3d9af-129">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="3d9af-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3d9af-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="3d9af-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

