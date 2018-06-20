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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d9a15abc05bf0f0a6fef35dd489f12925b88014a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800991"
---
# <a name="imsgserviceadmincopymsgservice"></a><span data-ttu-id="6b7ae-103">IMsgServiceAdmin::CopyMsgService</span><span class="sxs-lookup"><span data-stu-id="6b7ae-103">IMsgServiceAdmin::CopyMsgService</span></span>

  
  
<span data-ttu-id="6b7ae-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b7ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b7ae-105">メッセージ サービスをプロファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-105">Copies a message service into a profile.</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="6b7ae-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6b7ae-106">Parameters</span></span>

 <span data-ttu-id="6b7ae-107">_lpUID_</span><span class="sxs-lookup"><span data-stu-id="6b7ae-107">_lpUID_</span></span>
  
> <span data-ttu-id="6b7ae-108">[in]コピーするのにはメッセージ サービスの一意の識別子を格納する[MAPIUID](mapiuid.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier of the message service to copy.</span></span> 
    
 <span data-ttu-id="6b7ae-109">_lpszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="6b7ae-109">_lpszDisplayName_</span></span>
  
> <span data-ttu-id="6b7ae-110">[in]このパラメーターは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-110">[in] This parameter has been deprecated.</span></span> 
    
 <span data-ttu-id="6b7ae-111">_lpInterfaceToCopy_</span><span class="sxs-lookup"><span data-stu-id="6b7ae-111">_lpInterfaceToCopy_</span></span>
  
> <span data-ttu-id="6b7ae-112">[in]コピーするのにはメッセージ サービスのプロファイル セクションにアクセスするためのインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-112">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the profile section of the message service to copy.</span></span> <span data-ttu-id="6b7ae-113">NULL を渡すことは、標準のプロファイルで、 [IProfSect](iprofsectimapiprop.md)、使っているインターフェイスになります。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-113">Passing NULL results in the standard profile section interface, [IProfSect](iprofsectimapiprop.md), being used.</span></span>
    
 <span data-ttu-id="6b7ae-114">_lpInterfaceDst_</span><span class="sxs-lookup"><span data-stu-id="6b7ae-114">_lpInterfaceDst_</span></span>
  
> <span data-ttu-id="6b7ae-115">[in]_LpObjectDst_パラメーターが指すオブジェクトへのアクセスに使用するインターフェイスを表す IID へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-115">[in] A pointer to the IID that represents the interface to be used to access the object pointed to by the  _lpObjectDst_ parameter.</span></span> <span data-ttu-id="6b7ae-116">パラメーターに NULL は、セッション、 [IMAPISession](imapisessioniunknown.md)、使っているインターフェイスになります。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-116">Passing NULL results in the session interface, [IMAPISession](imapisessioniunknown.md), being used.</span></span> <span data-ttu-id="6b7ae-117">IID_IMsgServiceAdmin に、 _lpInterfaceDst_パラメーターを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-117">The  _lpInterfaceDst_ parameter can also be set to IID_IMsgServiceAdmin.</span></span> 
    
 <span data-ttu-id="6b7ae-118">_lpObjectDst_</span><span class="sxs-lookup"><span data-stu-id="6b7ae-118">_lpObjectDst_</span></span>
  
> <span data-ttu-id="6b7ae-119">[in]セッションまたはメッセージ サービスの管理オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-119">[in] A pointer to a pointer to a session or message service administration object.</span></span> <span data-ttu-id="6b7ae-120">オブジェクトの種類は、 _lpInterfaceDst_に渡されるインターフェイス識別子に対応します。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-120">The type of object should correspond to the interface identifier passed in  _lpInterfaceDst_.</span></span> <span data-ttu-id="6b7ae-121">有効なオブジェクトのポインターは、LPMAPISESSION および LPSERVICEADMIN です。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-121">Valid object pointers are LPMAPISESSION and LPSERVICEADMIN.</span></span>
    
 <span data-ttu-id="6b7ae-122">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6b7ae-122">_ulUIParam_</span></span>
  
> <span data-ttu-id="6b7ae-123">[in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-123">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span>
    
 <span data-ttu-id="6b7ae-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b7ae-124">_ulFlags_</span></span>
  
> <span data-ttu-id="6b7ae-125">[in]メッセージ サービスをコピーする方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-125">[in] A bitmask of flags that controls how the message service is copied.</span></span> <span data-ttu-id="6b7ae-126">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-126">The following flags can be set:</span></span>
    
<span data-ttu-id="6b7ae-127">SERVICE_UI_ALWAYS</span><span class="sxs-lookup"><span data-stu-id="6b7ae-127">SERVICE_UI_ALWAYS</span></span> 
  
> <span data-ttu-id="6b7ae-128">要求をメッセージ サービスは、構成のプロパティ シートを常に表示します。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-128">Requests that the message service always display a configuration property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b7ae-129">�߂�l</span><span class="sxs-lookup"><span data-stu-id="6b7ae-129">Return value</span></span>

<span data-ttu-id="6b7ae-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b7ae-130">S_OK</span></span> 
  
> <span data-ttu-id="6b7ae-131">メッセージ サービスは正常にコピーされました。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-131">The message service was successfully copied.</span></span>
    
<span data-ttu-id="6b7ae-132">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="6b7ae-132">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="6b7ae-133">メッセージ サービスは既にプロファイルに、それ自身の複数のインスタンスを許可しません。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-133">The message service is already in the profile and does not allow multiple instances of itself.</span></span>
    
<span data-ttu-id="6b7ae-134">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="6b7ae-134">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="6b7ae-135">_LpUID_で示される**MAPIUID**は、既存のメッセージ サービスを参照していません。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-135">The **MAPIUID** pointed to by  _lpUID_ does not refer to an existing message service.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b7ae-136">備考</span><span class="sxs-lookup"><span data-stu-id="6b7ae-136">Remarks</span></span>

<span data-ttu-id="6b7ae-137">**IMsgServiceAdmin::CopyMsgService**メソッドは、メッセージ サービスをアクティブなプロファイルまたは別のプロファイル、プロファイルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-137">The **IMsgServiceAdmin::CopyMsgService** method copies a message service into a profile, either the active profile or another profile.</span></span> <span data-ttu-id="6b7ae-138">コピーするメッセージ サービスを含むプロファイルと変換先は、同じプロファイルを使用するはありませんが、ことができます。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-138">The profile that contains the message service to be copied and the destination do not have to be the same profile, but they can be.</span></span> 
  
<span data-ttu-id="6b7ae-139">コピー操作は、メッセージ サービスのエントリ ポイント関数は呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-139">The message service's entry point function is not called for a copy operation.</span></span> <span data-ttu-id="6b7ae-140">コピーしたメッセージ サービスには、元のと同じ構成設定があります。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-140">The copied message service has the same configuration settings as its original.</span></span> <span data-ttu-id="6b7ae-141">クライアントはこれらの設定を変更するのには、 [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b7ae-141">To change these settings, a client should call the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b7ae-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="6b7ae-142">See also</span></span>



[<span data-ttu-id="6b7ae-143">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="6b7ae-143">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="6b7ae-144">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6b7ae-144">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="6b7ae-145">IMsgServiceAdmin: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b7ae-145">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

