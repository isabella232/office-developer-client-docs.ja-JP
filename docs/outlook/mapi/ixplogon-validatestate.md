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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a3469e6baacb52938b870ca87d824bf640a8a88f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439486"
---
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="cdc18-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cdc18-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="cdc18-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdc18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdc18-105">トランスポートプロバイダーの外部の状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="cdc18-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="cdc18-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cdc18-106">Parameters</span></span>

 <span data-ttu-id="cdc18-107">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="cdc18-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="cdc18-108">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="cdc18-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="cdc18-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cdc18-109">_ulFlags_</span></span>
  
> <span data-ttu-id="cdc18-110">順番状態チェックの実行方法と状態チェックの結果を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="cdc18-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="cdc18-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="cdc18-111">The following flags can be set:</span></span>
    
<span data-ttu-id="cdc18-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="cdc18-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="cdc18-113">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cdc18-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="cdc18-114">トランスポートプロバイダーは、操作を続行するか、操作を中止して MAPI_E_USER_CANCELED を返すかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="cdc18-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="cdc18-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="cdc18-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="cdc18-116">MAPI スプーラーに[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すことによって、現在読み込まれているトランスポートプロバイダーの状態を検証します。</span><span class="sxs-lookup"><span data-stu-id="cdc18-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="cdc18-117">また、このフラグを使用すると、MAPI スプーラーは、クライアントアプリケーションがログオフしてから再度ログオンすることなく、重要なトランスポートプロバイダーのエラーを修正する機会を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="cdc18-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="cdc18-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="cdc18-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="cdc18-119">ユーザーが接続操作を選択しました。</span><span class="sxs-lookup"><span data-stu-id="cdc18-119">The user selected a connect operation.</span></span> <span data-ttu-id="cdc18-120">このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグと共に使用すると、接続アクションはキャッシュなしで行われます。</span><span class="sxs-lookup"><span data-stu-id="cdc18-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="cdc18-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="cdc18-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="cdc18-122">ユーザーが切断操作を選択しました。</span><span class="sxs-lookup"><span data-stu-id="cdc18-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="cdc18-123">このフラグが REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE で使用されている場合、disconnect 操作はキャッシュなしで行われます。</span><span class="sxs-lookup"><span data-stu-id="cdc18-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="cdc18-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cdc18-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cdc18-125">ヘッダーキャッシュテーブル内のエントリを処理する必要があり、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたすべてのメッセージをダウンロードして、MSGSTATUS_REMOTE_DELETE フラグでマークされたすべてのメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc18-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="cdc18-126">MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE の両方が設定されたメッセージは移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc18-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="cdc18-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="cdc18-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="cdc18-128">メッセージヘッダーの新しいリストがダウンロードされ、すべてのメッセージ状態マーキングフラグがクリアされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc18-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="cdc18-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="cdc18-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="cdc18-130">トランスポートプロバイダーがユーザーインターフェイスを表示できないようにします。</span><span class="sxs-lookup"><span data-stu-id="cdc18-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cdc18-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="cdc18-131">Return value</span></span>

<span data-ttu-id="cdc18-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="cdc18-132">S_OK</span></span> 
  
> <span data-ttu-id="cdc18-133">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="cdc18-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="cdc18-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="cdc18-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="cdc18-135">別の操作が進行中です。完了することが許可されているか、この操作を実行する前に停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc18-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="cdc18-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cdc18-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="cdc18-137">関係するリモートトランスポートプロバイダーはユーザーインターフェイスをサポートしておらず、クライアントアプリケーション自体にダイアログボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cdc18-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="cdc18-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="cdc18-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="cdc18-139">ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cdc18-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cdc18-140">注釈</span><span class="sxs-lookup"><span data-stu-id="cdc18-140">Remarks</span></span>

<span data-ttu-id="cdc18-141">MAPI スプーラーは、 **IXPLogon:: validatestate**メソッドを呼び出して、ステータスオブジェクトの[imapistatus:: validatestate](imapistatus-validatestate.md)メソッドへの呼び出しをサポートします。</span><span class="sxs-lookup"><span data-stu-id="cdc18-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="cdc18-142">トランスポートプロバイダーは、 **IXPLogon:: validatestate**呼び出しに応答する必要があります。これは、MAPI スプーラーが現在のログオンセッションの状態オブジェクトを開いており、そのオブジェクトに対して**imapistatus:: validatestate**を呼び出した場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="cdc18-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="cdc18-143">**imapistatus:: validatestate**の実装をサポートするために、MAPI スプーラーは、プロファイルセッションで実行されているすべてのアクティブなトランスポートプロバイダーのすべてのログオンオブジェクトに対して**IXPLogon:: validatestate**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cdc18-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cdc18-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="cdc18-144">See also</span></span>



[<span data-ttu-id="cdc18-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="cdc18-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="cdc18-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="cdc18-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="cdc18-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cdc18-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

