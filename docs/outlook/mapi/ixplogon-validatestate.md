---
title: IXPLogonValidateState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.ValidateState
api_type:
- COM
ms.assetid: c3649daa-cba1-48e3-9ffb-069c1bcf8228
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 165fe3a72060e88dc34d8153c13ae58bcbd9ae0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801283"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="eaaee-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="eaaee-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="eaaee-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eaaee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eaaee-105">トランスポート プロバイダーの外部の状況をチェックします。</span><span class="sxs-lookup"><span data-stu-id="eaaee-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="eaaee-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="eaaee-106">Parameters</span></span>

 <span data-ttu-id="eaaee-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="eaaee-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="eaaee-108">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="eaaee-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="eaaee-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="eaaee-109">_ulFlags_</span></span>
  
> <span data-ttu-id="eaaee-110">[in]状態チェックの実行方法を制御するフラグのビットマスクと状態の結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="eaaee-111">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="eaaee-111">The following flags can be set:</span></span>
    
<span data-ttu-id="eaaee-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="eaaee-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="eaaee-113">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="eaaee-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="eaaee-114">トランスポート プロバイダーは、操作の操作を続行するオプションか、操作を中止して MAPI_E_USER_CANCELED を返します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="eaaee-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="eaaee-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="eaaee-116">MAPI スプーラーを無効に、 [IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すことで、現在読み込まれているトランスポート プロバイダーの状態を検証します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="eaaee-117">このフラグでは、いったんログオフして再度ログオンするクライアント アプリケーションを強制することのないトランスポート プロバイダーの重要なエラーを修正すること、MAPI スプーラーも提供します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="eaaee-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="eaaee-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="eaaee-119">ユーザーは、接続操作を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-119">The user selected a connect operation.</span></span> <span data-ttu-id="eaaee-120">REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグを指定してこのフラグを使用する場合は、キャッシュを使用しない接続の動作が発生します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="eaaee-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="eaaee-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="eaaee-122">ユーザーは、切断操作を選択します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="eaaee-123">このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE を使用する場合は、キャッシュを使用しない切断操作が発生します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="eaaee-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="eaaee-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="eaaee-125">ヘッダー キャッシュ テーブル内のエントリを処理する必要があります、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたすべてのメッセージをダウンロードするか、および、MSGSTATUS_REMOTE_DELETE フラグでマークされたすべてのメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaaee-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="eaaee-126">MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE の設定の両方を持つメッセージを移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaaee-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="eaaee-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="eaaee-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="eaaee-128">メッセージ ヘッダーの新しいリストをダウンロードするか、およびフラグをマークするすべてのメッセージの状態をクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaaee-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="eaaee-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="eaaee-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="eaaee-130">トランスポート プロバイダーが、ユーザー インターフェイスを表示するを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="eaaee-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eaaee-131">�߂�l</span><span class="sxs-lookup"><span data-stu-id="eaaee-131">Return value</span></span>

<span data-ttu-id="eaaee-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="eaaee-132">S_OK</span></span> 
  
> <span data-ttu-id="eaaee-133">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="eaaee-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="eaaee-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="eaaee-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="eaaee-135">別の操作が実行中です。完了するために許可するか、この操作を実行しようとする前に停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaaee-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="eaaee-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="eaaee-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="eaaee-137">リモート トランスポート プロバイダーの関連するが、ユーザー インターフェイスをサポートしていませんし、クライアント アプリケーションでは、ダイアログ ボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaaee-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="eaaee-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="eaaee-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="eaaee-139">ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="eaaee-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="eaaee-140">注釈</span><span class="sxs-lookup"><span data-stu-id="eaaee-140">Remarks</span></span>

<span data-ttu-id="eaaee-141">MAPI スプーラーは、状態オブジェクトの[IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドの呼び出しをサポートするために**IXPLogon::ValidateState**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="eaaee-142">トランスポート プロバイダーは、正確に場合と、MAPI スプーラーが現在のログオン セッションの状態のオブジェクトを開くし、そのオブジェクトに**IMAPIStatus::ValidateState**と呼ばれる**IXPLogon::ValidateState**の呼び出しに応答します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="eaaee-143">**IMAPIStatus::ValidateState**の実装をサポートするには、MAPI スプーラーは、ログオン オブジェクトのすべてのプロファイル セッションで実行されているすべてのアクティブなトランスポート プロバイダーの**IXPLogon::ValidateState**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="eaaee-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eaaee-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="eaaee-144">See also</span></span>



[<span data-ttu-id="eaaee-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="eaaee-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="eaaee-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="eaaee-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="eaaee-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eaaee-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

