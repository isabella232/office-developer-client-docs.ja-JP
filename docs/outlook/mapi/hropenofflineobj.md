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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ac6584819b5dfa96a5f7816f1d77b89323e3eaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800332"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="d5169-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="d5169-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="d5169-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d5169-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d5169-105">特定のプロファイルでオフラインのオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="d5169-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d5169-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d5169-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5169-107">によってエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="d5169-107">Exported by:</span></span>  <br/> |<span data-ttu-id="d5169-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="d5169-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="d5169-109">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d5169-109">Called by:</span></span>  <br/> |<span data-ttu-id="d5169-110">クライアント</span><span class="sxs-lookup"><span data-stu-id="d5169-110">Client</span></span>  <br/> |
|<span data-ttu-id="d5169-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="d5169-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="d5169-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="d5169-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="d5169-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="d5169-113">Parameters</span></span>

 <span data-ttu-id="d5169-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="d5169-114">_ulReserved_</span></span>
  
> <span data-ttu-id="d5169-115">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="d5169-115">[in] This parameter is not used.</span></span> <span data-ttu-id="d5169-116">0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5169-116">It must be 0.</span></span>
    
 <span data-ttu-id="d5169-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="d5169-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="d5169-118">[in]オフライン オブジェクトが適用されるプロファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="d5169-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="d5169-119">は、Unicode で表現する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5169-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="d5169-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="d5169-120">_pGUID_</span></span>
  
> <span data-ttu-id="d5169-121">[in]オフラインの他のオブジェクトからこのオブジェクトを一意に識別に使用できる GUID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5169-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="d5169-122">**GUID_GlobalState**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5169-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="d5169-123">_保持_</span><span class="sxs-lookup"><span data-stu-id="d5169-123">_pReserved_</span></span>
  
> <span data-ttu-id="d5169-124">[in]このパラメーターは使用されません。</span><span class="sxs-lookup"><span data-stu-id="d5169-124">[in] This parameter is not used.</span></span> <span data-ttu-id="d5169-125">**Null**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d5169-125">It must be **null**.</span></span>
    
 <span data-ttu-id="d5169-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="d5169-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="d5169-127">[out]要求されたオフライン オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d5169-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="d5169-128">呼び出し元がこのポインターを使ってアクセスするのには、 [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md)インターフェイスをオブジェクトがサポートするコールバックを検索して、それ用のコールバックを設定します。</span><span class="sxs-lookup"><span data-stu-id="d5169-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="d5169-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="d5169-129">Return values</span></span>

<span data-ttu-id="d5169-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="d5169-130">S_OK</span></span> 
  
- <span data-ttu-id="d5169-131">関数の呼び出しが成功します。</span><span class="sxs-lookup"><span data-stu-id="d5169-131">The function call is successful.</span></span>
    
<span data-ttu-id="d5169-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d5169-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="d5169-133">関数呼び出しが失敗しました。</span><span class="sxs-lookup"><span data-stu-id="d5169-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d5169-134">備考</span><span class="sxs-lookup"><span data-stu-id="d5169-134">Remarks</span></span>

<span data-ttu-id="d5169-135">これは、クライアントでクライアントは、特定のプロファイルの接続状態の変更の通知を希望する場合は、最初の呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="d5169-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="d5169-136">**HrOpenOfflineObj**を呼び出すと、時に、クライアントは、 **IMAPIOfflineMgr**をサポートしているオフラインのオブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="d5169-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="d5169-137">クライアントを使用して[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md))、オブジェクトがサポートするコールバックの種類を確認し、コールバックを (を使用して設定[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md))。</span><span class="sxs-lookup"><span data-stu-id="d5169-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="d5169-138">Msmapi32.dll のこの関数のアドレスを検索するには、 [GetProcAddress](http://msdn.microsoft.com/ja-jp/library/ms683212.aspx)を使用して、プロシージャ名として**HrOpenOfflineObj@20**を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5169-138">When using [GetProcAddress](http://msdn.microsoft.com/ja-jp/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="d5169-139">**HrOpenOfflineObj**は、COM アドインおよび Exchange クライアント拡張機能が Outlook のプロセス内で実行中の MAPI プロバイダーは、クライアントに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="d5169-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="d5169-140">それ以外の場合、 **HrOpenOfflineObj**は**MAPI_E_NOT_FOUND**を返します。</span><span class="sxs-lookup"><span data-stu-id="d5169-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d5169-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="d5169-141">See also</span></span>



[<span data-ttu-id="d5169-142">IMAPIOffline: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d5169-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="d5169-143">IMAPIOfflineMgr: IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="d5169-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="d5169-144">オフラインの状態の API について</span><span class="sxs-lookup"><span data-stu-id="d5169-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="d5169-145">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="d5169-145">MAPI Constants</span></span>](mapi-constants.md)

