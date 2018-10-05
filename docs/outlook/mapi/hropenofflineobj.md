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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395799"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="60296-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="60296-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="60296-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60296-105">特定のプロファイルでオフラインのオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="60296-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="60296-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="60296-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60296-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="60296-107">Exported by:</span></span>  <br/> |<span data-ttu-id="60296-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="60296-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="60296-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="60296-109">Called by:</span></span>  <br/> |<span data-ttu-id="60296-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="60296-110">Client</span></span>  <br/> |
|<span data-ttu-id="60296-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="60296-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="60296-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="60296-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="60296-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="60296-113">Parameters</span></span>

 <span data-ttu-id="60296-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="60296-114">_ulReserved_</span></span>
  
> <span data-ttu-id="60296-115">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="60296-115">[in] This parameter is not used.</span></span> <span data-ttu-id="60296-116">0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="60296-116">It must be 0.</span></span>
    
 <span data-ttu-id="60296-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="60296-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="60296-118">[in]オフライン オブジェクトが適用されるプロファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="60296-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="60296-119">は、Unicode で表現する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60296-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="60296-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="60296-120">_pGUID_</span></span>
  
> <span data-ttu-id="60296-121">[in]オフラインの他のオブジェクトからこのオブジェクトを一意に識別に使用できる GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="60296-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="60296-122">**GUID_GlobalState**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="60296-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="60296-123">_保持_</span><span class="sxs-lookup"><span data-stu-id="60296-123">_pReserved_</span></span>
  
> <span data-ttu-id="60296-124">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="60296-124">[in] This parameter is not used.</span></span> <span data-ttu-id="60296-125">**Null**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="60296-125">It must be **null**.</span></span>
    
 <span data-ttu-id="60296-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="60296-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="60296-127">[out]要求されたオフライン オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="60296-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="60296-128">呼び出し元がこのポインターを使ってアクセスするのには、 [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md)インターフェイスをオブジェクトがサポートするコールバックを検索して、それ用のコールバックを設定します。</span><span class="sxs-lookup"><span data-stu-id="60296-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="60296-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="60296-129">Return values</span></span>

<span data-ttu-id="60296-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="60296-130">S_OK</span></span> 
  
- <span data-ttu-id="60296-131">関数の呼び出しが成功します。</span><span class="sxs-lookup"><span data-stu-id="60296-131">The function call is successful.</span></span>
    
<span data-ttu-id="60296-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="60296-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="60296-133">関数呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="60296-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="60296-134">備考</span><span class="sxs-lookup"><span data-stu-id="60296-134">Remarks</span></span>

<span data-ttu-id="60296-135">これは、クライアントでクライアントは、特定のプロファイルの接続状態の変更の通知を希望する場合は、最初の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="60296-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="60296-136">**HrOpenOfflineObj**を呼び出すと、時に、クライアントは、 **IMAPIOfflineMgr**をサポートしているオフラインのオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="60296-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="60296-137">クライアントを使用して[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md))、オブジェクトがサポートするコールバックの種類を確認し、コールバックを (を使用して設定[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md))。</span><span class="sxs-lookup"><span data-stu-id="60296-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="60296-138">Msmapi32.dll のこの関数のアドレスを検索するには、 [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)を使用して、プロシージャ名として**HrOpenOfflineObj@20**を指定します。</span><span class="sxs-lookup"><span data-stu-id="60296-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="60296-139">**HrOpenOfflineObj**は、COM アドインおよび Exchange クライアント拡張機能が Outlook のプロセス内で実行中の MAPI プロバイダーは、クライアントに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="60296-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="60296-140">それ以外の場合、 **HrOpenOfflineObj**は**MAPI_E_NOT_FOUND**を返します。</span><span class="sxs-lookup"><span data-stu-id="60296-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="60296-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="60296-141">See also</span></span>



[<span data-ttu-id="60296-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="60296-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="60296-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="60296-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="60296-144">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="60296-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="60296-145">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="60296-145">MAPI Constants</span></span>](mapi-constants.md)

