---
title: IMsgServiceAdminCopyMsgService
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CopyMsgService
api_type:
- COM
ms.assetid: a13c6757-358f-421a-9a76-de7483501613
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 72b4ab1fec10b2e91c7609af6644a54d29ed5e02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432122"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="a2b35-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="a2b35-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="a2b35-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a2b35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a2b35-105">メッセージ サービスをプロファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a2b35-105">Copies a message service into a profile.</span></span> 
  
```cpp
HRESULT CopyMsgService(
  LPMAPIUID lpUID,
  LPSTR lpszDisplayName,
  LPCIID lpInterfaceToCopy,
  LPCIID lpInterfaceDst,
  LPVOID lpObjectDst,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a2b35-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a2b35-106">Parameters</span></span>

 <span data-ttu-id="a2b35-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="a2b35-107">_lpUID_</span></span>
  
> <span data-ttu-id="a2b35-108">[in]コピーするメッセージ サービスの一意の識別子を含む [MAPIUID](mapiuid.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a2b35-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="a2b35-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="a2b35-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="a2b35-110">[in]このパラメーターは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="a2b35-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="a2b35-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="a2b35-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="a2b35-112">[in]コピーするメッセージ サービスのプロファイル セクションにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a2b35-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="a2b35-113">NULL を渡す場合、標準のプロファイル セクション インターフェイス [IProfSect](iprofsectimapiprop.md)が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2b35-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="a2b35-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="a2b35-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="a2b35-115">[in]  _lpObjectDst_ パラメーターが指すオブジェクトにアクセスするために使用するインターフェイスを表す IID へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a2b35-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="a2b35-116">NULL を渡す場合、セッション インターフェイス [IMAPISession](imapisessioniunknown.md)が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2b35-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="a2b35-117">_lpInterfaceDst_ パラメーターは、このパラメーターにIID_IMsgServiceAdmin。</span><span class="sxs-lookup"><span data-stu-id="a2b35-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="a2b35-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="a2b35-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="a2b35-119">[in]セッションまたはメッセージ サービス管理オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a2b35-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="a2b35-120">オブジェクトの種類は、lpInterfaceDst で渡されるインターフェイス識別子  _に対応する必要があります_。</span><span class="sxs-lookup"><span data-stu-id="a2b35-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="a2b35-121">有効なオブジェクト ポインターは、LPMAPISESSION と LPSERVICEADMIN です。</span><span class="sxs-lookup"><span data-stu-id="a2b35-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="a2b35-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="a2b35-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="a2b35-123">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="a2b35-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="a2b35-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a2b35-124">_ulFlags_</span></span>
  
> <span data-ttu-id="a2b35-125">[in]メッセージ サービスのコピー方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a2b35-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="a2b35-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2b35-126">The following flags can be set:</span></span>
    
<span data-ttu-id="a2b35-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="a2b35-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="a2b35-128">メッセージ サービスが常に構成プロパティ シートを表示する要求。</span><span class="sxs-lookup"><span data-stu-id="a2b35-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a2b35-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="a2b35-129">Return value</span></span>

<span data-ttu-id="a2b35-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2b35-130">S_OK</span></span> 
  
> <span data-ttu-id="a2b35-131">メッセージ サービスが正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="a2b35-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="a2b35-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="a2b35-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="a2b35-133">メッセージ サービスは既にプロファイル内に存在し、それ自体の複数のインスタンスを許可しません。</span><span class="sxs-lookup"><span data-stu-id="a2b35-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="a2b35-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a2b35-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a2b35-135">**lpUID が** 指す _MAPIUID は_、既存のメッセージ サービスを参照していない。</span><span class="sxs-lookup"><span data-stu-id="a2b35-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a2b35-136">注釈</span><span class="sxs-lookup"><span data-stu-id="a2b35-136">Remarks</span></span>

<span data-ttu-id="a2b35-137">**IMsgServiceAdmin::CopyMsgService** メソッドは、メッセージ サービスをアクティブ なプロファイルまたは別のプロファイルのどちらかのプロファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="a2b35-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="a2b35-138">コピーするメッセージ サービスとコピー先を含むプロファイルは、同じプロファイルである必要は一方で、同じプロファイルである必要は生じ得る。</span><span class="sxs-lookup"><span data-stu-id="a2b35-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="a2b35-139">コピー操作では、メッセージ サービスのエントリ ポイント関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="a2b35-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="a2b35-140">コピーされたメッセージ サービスの構成設定は、元のメッセージ サービスと同じです。</span><span class="sxs-lookup"><span data-stu-id="a2b35-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="a2b35-141">これらの設定を変更するには、クライアントが [IMsgServiceAdmin::ConfigureMsgService メソッドを呼び出す必要](imsgserviceadmin-configuremsgservice.md) があります。</span><span class="sxs-lookup"><span data-stu-id="a2b35-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a2b35-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="a2b35-142">See also</span></span>



[<span data-ttu-id="a2b35-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="a2b35-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="a2b35-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="a2b35-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="a2b35-145">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2b35-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

