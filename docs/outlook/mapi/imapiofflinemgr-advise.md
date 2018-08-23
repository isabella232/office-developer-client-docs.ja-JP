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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e0c8c4c6251581506c7bdd78c009bb12e8291c81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586936"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="29b22-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="29b22-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="29b22-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29b22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29b22-105">オフライン オブジェクトに対してコールバックを受信するようにクライアントを登録します。</span><span class="sxs-lookup"><span data-stu-id="29b22-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="29b22-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="29b22-106">Parameters</span></span>

 <span data-ttu-id="29b22-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="29b22-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="29b22-108">[in]動作を変更するフラグです。</span><span class="sxs-lookup"><span data-stu-id="29b22-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="29b22-109">MAPIOFFLINE_ADVISE_DEFAULT の値のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="29b22-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="29b22-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="29b22-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="29b22-111">[in]コールバックの種類に関する情報やその他の詳細については、呼び出し元、コールバック、コールバック インターフェイスを表示する場合。</span><span class="sxs-lookup"><span data-stu-id="29b22-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="29b22-112">クライアントの呼び出し元にコールバックの後続の通知を送信することで Outlook を使用するクライアントのトークンも含まれています。</span><span class="sxs-lookup"><span data-stu-id="29b22-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="29b22-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="29b22-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="29b22-114">[out]その後、オブジェクトのコールバックをキャンセルするクライアントの呼び出し元に返されるアドバイスのトークンです。</span><span class="sxs-lookup"><span data-stu-id="29b22-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29b22-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="29b22-115">Return value</span></span>

<span data-ttu-id="29b22-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="29b22-116">S_OK</span></span>
  
> <span data-ttu-id="29b22-117">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="29b22-117">The call was successful.</span></span>
    
<span data-ttu-id="29b22-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="29b22-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="29b22-119">無効なパラメーターが指定されています。</span><span class="sxs-lookup"><span data-stu-id="29b22-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="29b22-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="29b22-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="29b22-121">*PAdviseInfo*で指定されたコールバック インターフェイスが有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="29b22-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="29b22-122">注釈</span><span class="sxs-lookup"><span data-stu-id="29b22-122">Remarks</span></span>

<span data-ttu-id="29b22-123">**[HrOpenOfflineObj](hropenofflineobj.md)** を使用してオフラインのオブジェクトを開くには、クライアントは、 **IMAPIOfflineMgr**をサポートしているオフラインのオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="29b22-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="29b22-124">クライアントは、 **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を使用して、オブジェクトがサポートするコールバックの種類を確認できます。</span><span class="sxs-lookup"><span data-stu-id="29b22-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="29b22-125">クライアントには、型とその他の詳細が、そのオブジェクトについては、このようなコールバックを受信するように登録するのには**IMAPIOfflineMgr::Advise**を呼び出し、コールバックを決定できます。</span><span class="sxs-lookup"><span data-stu-id="29b22-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="29b22-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="29b22-126">See also</span></span>



[<span data-ttu-id="29b22-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="29b22-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="29b22-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="29b22-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="29b22-129">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="29b22-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="29b22-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="29b22-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

