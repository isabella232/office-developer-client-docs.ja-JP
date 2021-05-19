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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347748"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="12209-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="12209-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="12209-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12209-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12209-105">指定したプロファイルに基づいてオフライン オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="12209-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="12209-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="12209-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12209-107">次の方法でエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="12209-107">Exported by:</span></span>  <br/> |<span data-ttu-id="12209-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="12209-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="12209-109">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="12209-109">Called by:</span></span>  <br/> |<span data-ttu-id="12209-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="12209-110">Client</span></span>  <br/> |
|<span data-ttu-id="12209-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="12209-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="12209-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="12209-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="12209-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="12209-113">Parameters</span></span>

 <span data-ttu-id="12209-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="12209-114">_ulReserved_</span></span>
  
> <span data-ttu-id="12209-115">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="12209-115">[in] This parameter is not used.</span></span> <span data-ttu-id="12209-116">0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="12209-116">It must be 0.</span></span>
    
 <span data-ttu-id="12209-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="12209-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="12209-118">[in]オフライン オブジェクトのプロファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="12209-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="12209-119">Unicode で表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="12209-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="12209-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="12209-120">_pGUID_</span></span>
  
> <span data-ttu-id="12209-121">[in]他のオフライン オブジェクトからこのオブジェクトを一意に識別するために使用できる GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="12209-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="12209-122">これは **、次の** GUID_GlobalState。</span><span class="sxs-lookup"><span data-stu-id="12209-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="12209-123">_pReserved_</span><span class="sxs-lookup"><span data-stu-id="12209-123">_pReserved_</span></span>
  
> <span data-ttu-id="12209-124">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="12209-124">[in] This parameter is not used.</span></span> <span data-ttu-id="12209-125">null である **必要があります**。</span><span class="sxs-lookup"><span data-stu-id="12209-125">It must be **null**.</span></span>
    
 <span data-ttu-id="12209-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="12209-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="12209-127">[out]要求されたオフライン オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="12209-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="12209-128">呼び出し元は、このポインターを使用して [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) インターフェイスにアクセスして、このオブジェクトがサポートするコールバックを検索し、コールバックを設定できます。</span><span class="sxs-lookup"><span data-stu-id="12209-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="12209-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="12209-129">Return values</span></span>

<span data-ttu-id="12209-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="12209-130">S_OK</span></span> 
  
- <span data-ttu-id="12209-131">関数呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="12209-131">The function call is successful.</span></span>
    
<span data-ttu-id="12209-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="12209-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="12209-133">関数呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="12209-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12209-134">注釈</span><span class="sxs-lookup"><span data-stu-id="12209-134">Remarks</span></span>

<span data-ttu-id="12209-135">これは、クライアントが特定のプロファイルの接続状態の変更を通知する場合にクライアントが行う最初の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="12209-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="12209-136">**HrOpenOfflineObj を呼び** 出す際に、クライアントは **IMAPIOfflineMgr** をサポートするオフライン オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="12209-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="12209-137">クライアントは [、(IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)を使用して) オブジェクトでサポートされるコールバックの種類を確認し [、(IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)を使用して) コールバックを設定できます。</span><span class="sxs-lookup"><span data-stu-id="12209-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="12209-138">[GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx)を使用してこの関数のアドレスを検索する場合は、プロシージャmsmapi32.dllとして **HrOpenOfflineObj@20を指定** します。</span><span class="sxs-lookup"><span data-stu-id="12209-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="12209-139">**HrOpenOfflineObj** は、MAPI プロバイダー、COM アドイン、および Exchange プロセス内で実行されているクライアントOutlook機能します。</span><span class="sxs-lookup"><span data-stu-id="12209-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="12209-140">それ以外の **場合、HrOpenOfflineObj** は **次MAPI_E_NOT_FOUNDします**。</span><span class="sxs-lookup"><span data-stu-id="12209-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="12209-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="12209-141">See also</span></span>



[<span data-ttu-id="12209-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="12209-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="12209-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="12209-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="12209-144">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="12209-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="12209-145">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="12209-145">MAPI Constants</span></span>](mapi-constants.md)

