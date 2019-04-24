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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321428"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="cf1cc-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="cf1cc-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="cf1cc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf1cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf1cc-105">クライアントを、オフラインオブジェクトのコールバックを受信するように登録します。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="cf1cc-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cf1cc-106">Parameters</span></span>

 <span data-ttu-id="cf1cc-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf1cc-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="cf1cc-108">順番動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="cf1cc-109">MAPIOFFLINE_ADVISE_DEFAULT の値のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="cf1cc-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="cf1cc-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="cf1cc-111">順番コールバックの種類、コールバックを受信するタイミング、発信者のコールバックインターフェイス、およびその他の詳細についての情報。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="cf1cc-112">また、このメソッドには、クライアントの発信者に後続の通知コールバックを送信するために Outlook が使用するクライアントトークンも含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="cf1cc-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="cf1cc-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="cf1cc-114">読み上げその後、オブジェクトのコールバックをキャンセルするためにクライアントの呼び出し元に返されるアドバイズトークン。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf1cc-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="cf1cc-115">Return value</span></span>

<span data-ttu-id="cf1cc-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf1cc-116">S_OK</span></span>
  
> <span data-ttu-id="cf1cc-117">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-117">The call was successful.</span></span>
    
<span data-ttu-id="cf1cc-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cf1cc-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="cf1cc-119">無効なパラメーターが指定されています。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="cf1cc-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="cf1cc-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="cf1cc-121">*pAdviseInfo*で指定されているコールバックインターフェイスが無効です。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf1cc-122">解説</span><span class="sxs-lookup"><span data-stu-id="cf1cc-122">Remarks</span></span>

<span data-ttu-id="cf1cc-123">**[hroIMAPIOfflineMgr offlineobj](hropenofflineobj.md)** を使用してオフラインオブジェクトを開くときに、クライアントは、 \*\*\*\* をサポートするオフラインオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="cf1cc-124">クライアントは、 **[imapioffline:: getcapabilities](imapioffline-getcapabilities.md)** を使用して、オブジェクトでサポートされているコールバックの種類を確認できます。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="cf1cc-125">クライアントは、必要なコールバックに関する種類とその他の詳細を判断し、 **IMAPIOfflineMgr:: アドバイズ**に登録して、オブジェクトに関するそのようなコールバックを受信することができます。</span><span class="sxs-lookup"><span data-stu-id="cf1cc-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cf1cc-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf1cc-126">See also</span></span>



[<span data-ttu-id="cf1cc-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="cf1cc-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="cf1cc-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="cf1cc-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="cf1cc-129">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="cf1cc-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="cf1cc-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="cf1cc-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

