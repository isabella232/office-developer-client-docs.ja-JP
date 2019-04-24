---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347748"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="50fe6-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="50fe6-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="50fe6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50fe6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50fe6-105">特定のプロファイルに基づいてオフラインオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="50fe6-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="50fe6-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="50fe6-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50fe6-107">エクスポート対象:</span><span class="sxs-lookup"><span data-stu-id="50fe6-107">Exported by:</span></span>  <br/> |<span data-ttu-id="50fe6-108">msmapi32</span><span class="sxs-lookup"><span data-stu-id="50fe6-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="50fe6-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="50fe6-109">Called by:</span></span>  <br/> |<span data-ttu-id="50fe6-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="50fe6-110">Client</span></span>  <br/> |
|<span data-ttu-id="50fe6-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="50fe6-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="50fe6-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="50fe6-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="50fe6-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50fe6-113">Parameters</span></span>

 <span data-ttu-id="50fe6-114">_ulreserved_</span><span class="sxs-lookup"><span data-stu-id="50fe6-114">_ulReserved_</span></span>
  
> <span data-ttu-id="50fe6-115">順番このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="50fe6-115">[in] This parameter is not used.</span></span> <span data-ttu-id="50fe6-116">0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="50fe6-116">It must be 0.</span></span>
    
 <span data-ttu-id="50fe6-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="50fe6-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="50fe6-118">順番オフラインオブジェクトのプロファイルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="50fe6-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="50fe6-119">Unicode で表されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="50fe6-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="50fe6-120">_pguid_</span><span class="sxs-lookup"><span data-stu-id="50fe6-120">_pGUID_</span></span>
  
> <span data-ttu-id="50fe6-121">順番他のオフラインオブジェクトからこのオブジェクトを一意に識別するために使用できる GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="50fe6-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="50fe6-122">**GUID_GlobalState**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="50fe6-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="50fe6-123">_保持され_</span><span class="sxs-lookup"><span data-stu-id="50fe6-123">_pReserved_</span></span>
  
> <span data-ttu-id="50fe6-124">順番このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="50fe6-124">[in] This parameter is not used.</span></span> <span data-ttu-id="50fe6-125">**null**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="50fe6-125">It must be **null**.</span></span>
    
 <span data-ttu-id="50fe6-126">_ppofflineobj_</span><span class="sxs-lookup"><span data-stu-id="50fe6-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="50fe6-127">読み上げ要求されたオフラインオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="50fe6-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="50fe6-128">発信者はこのポインターを使用して[IMAPIOfflineMgr: imapioffline](imapiofflinemgrimapioffline.md)インターフェイスにアクセスし、このオブジェクトでサポートされているコールバックを検索し、そのためのコールバックを設定できます。</span><span class="sxs-lookup"><span data-stu-id="50fe6-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="50fe6-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="50fe6-129">Return values</span></span>

<span data-ttu-id="50fe6-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="50fe6-130">S_OK</span></span> 
  
- <span data-ttu-id="50fe6-131">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="50fe6-131">The function call is successful.</span></span>
    
<span data-ttu-id="50fe6-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="50fe6-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="50fe6-133">関数の呼び出しに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="50fe6-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50fe6-134">解説</span><span class="sxs-lookup"><span data-stu-id="50fe6-134">Remarks</span></span>

<span data-ttu-id="50fe6-135">これは、クライアントが特定のプロファイルの接続状態変更を通知する際にクライアントが行う最初の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="50fe6-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="50fe6-136">**hroIMAPIOfflineMgr offlineobj**を呼び出すと、クライアントは\*\*\*\* をサポートするオフラインオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="50fe6-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="50fe6-137">クライアントは、( [imapioffline:: getcapabilities](imapioffline-getcapabilities.md)を使用して) オブジェクトでサポートされているコールバックの種類を確認し、そのためのコールバックを設定します ( [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)を使用)。</span><span class="sxs-lookup"><span data-stu-id="50fe6-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="50fe6-138">[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)を使用して msmapi32 でこの関数のアドレスを検索する場合は、手順名として**hrolook offlineobj @ 20**を指定します。</span><span class="sxs-lookup"><span data-stu-id="50fe6-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="50fe6-139">**hroare offlineobj**は、Outlook プロセス内で実行されている MAPI プロバイダー、COM アドイン、および Exchange クライアント拡張機能であるクライアントに対してのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="50fe6-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="50fe6-140">それ以外の場合、 **hroMAPI_E_NOT_FOUND offlineobj**は\*\*\*\* を返します。</span><span class="sxs-lookup"><span data-stu-id="50fe6-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50fe6-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="50fe6-141">See also</span></span>



[<span data-ttu-id="50fe6-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50fe6-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="50fe6-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="50fe6-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="50fe6-144">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="50fe6-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="50fe6-145">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="50fe6-145">MAPI Constants</span></span>](mapi-constants.md)

