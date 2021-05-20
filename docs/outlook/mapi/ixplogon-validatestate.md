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
# <a name="ixplogonvalidatestate"></a><span data-ttu-id="0d3f7-103">IXPLogon::ValidateState</span><span class="sxs-lookup"><span data-stu-id="0d3f7-103">IXPLogon::ValidateState</span></span>

  
  
<span data-ttu-id="0d3f7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d3f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d3f7-105">トランスポート プロバイダーの外部状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-105">Checks the transport provider's external status.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0d3f7-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0d3f7-106">Parameters</span></span>

 <span data-ttu-id="0d3f7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0d3f7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0d3f7-108">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="0d3f7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d3f7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0d3f7-110">[in]状態チェックの実行方法と状態チェックの結果を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-110">[in] A bitmask of flags that controls how the status check is performed and the results of the status check.</span></span> <span data-ttu-id="0d3f7-111">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-111">The following flags can be set:</span></span>
    
<span data-ttu-id="0d3f7-112">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="0d3f7-112">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="0d3f7-113">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-113">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="0d3f7-114">トランスポート プロバイダーは、操作の作業を続行するか、操作を中止し、操作を返MAPI_E_USER_CANCELED。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-114">The transport provider has the option to continue working on the operation, or it can abort the operation and return MAPI_E_USER_CANCELED.</span></span> 
    
<span data-ttu-id="0d3f7-115">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="0d3f7-115">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="0d3f7-116">MAPI スプーラーが [IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッドを呼び出して、現在読み込まれているトランスポート プロバイダーの状態を検証します。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-116">Validates the state of currently loaded transport providers by causing the MAPI spooler to call their [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="0d3f7-117">また、このフラグを使用すると、MAPI スプーラーは、クライアント アプリケーションにログオフしてから再度ログオンすることなく、重大なトランスポート プロバイダーのエラーを修正できます。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-117">This flag also provides the MAPI spooler an opportunity to correct critical transport-provider failures without forcing client applications to log off and then log on again.</span></span> 
    
<span data-ttu-id="0d3f7-118">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="0d3f7-118">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="0d3f7-119">ユーザーが接続操作を選択しました。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-119">The user selected a connect operation.</span></span> <span data-ttu-id="0d3f7-120">このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHEと一緒に使用すると、接続アクションはキャッシュなしで実行されます。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-120">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connect action occurs without caching.</span></span>
    
<span data-ttu-id="0d3f7-121">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="0d3f7-121">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="0d3f7-122">ユーザーが切断操作を選択しました。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-122">The user selected a disconnect operation.</span></span> <span data-ttu-id="0d3f7-123">このフラグを使用して、REFRESH_XP_HEADER_CACHEまたはPROCESS_XP_HEADER_CACHEキャッシュせずに切断アクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-123">When this flag is used with REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE, the disconnect action occurs without caching.</span></span>
    
<span data-ttu-id="0d3f7-124">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="0d3f7-124">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="0d3f7-125">ヘッダー キャッシュ テーブル内のエントリを処理し、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたメッセージはすべてダウンロードし、MSGSTATUS_REMOTE_DELETE フラグでマークされたメッセージはすべて削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-125">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="0d3f7-126">設定されたメッセージとMSGSTATUS_REMOTE_DOWNLOAD設定MSGSTATUS_REMOTE_DELETEメッセージを移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-126">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="0d3f7-127">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="0d3f7-127">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="0d3f7-128">メッセージ ヘッダーの新しい一覧をダウンロードし、すべてのメッセージ状態マーキング フラグをクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-128">A new list of message headers should be downloaded, and all message status marking flags should be cleared.</span></span>
    
<span data-ttu-id="0d3f7-129">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="0d3f7-129">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="0d3f7-130">トランスポート プロバイダーがユーザー インターフェイスを表示しなかします。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-130">Prevents the transport provider from displaying a user interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d3f7-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="0d3f7-131">Return value</span></span>

<span data-ttu-id="0d3f7-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d3f7-132">S_OK</span></span> 
  
> <span data-ttu-id="0d3f7-133">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-133">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="0d3f7-134">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="0d3f7-134">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="0d3f7-135">別の操作が進行中です。完了を許可するか、この操作を試みる前に停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-135">Another operation is in progress; it should be allowed to complete, or it should be stopped before this operation is attempted.</span></span>
    
<span data-ttu-id="0d3f7-136">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0d3f7-136">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0d3f7-137">関連するリモート トランスポート プロバイダーはユーザー インターフェイスをサポートしていないので、クライアント アプリケーション自体がダイアログ ボックスを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-137">The remote transport provider involved does not support a user interface, and the client application itself should display the dialog box.</span></span>
    
<span data-ttu-id="0d3f7-138">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0d3f7-138">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0d3f7-139">通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-139">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0d3f7-140">注釈</span><span class="sxs-lookup"><span data-stu-id="0d3f7-140">Remarks</span></span>

<span data-ttu-id="0d3f7-141">MAPI スプーラーは **、IXPLogon::ValidateState** メソッドを呼び出して、STATUS オブジェクトの [IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドの呼び出しをサポートします。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-141">The MAPI spooler calls the **IXPLogon::ValidateState** method to support calls to the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method for the status object.</span></span> <span data-ttu-id="0d3f7-142">トランスポート プロバイダーは、MAPI スプーラーが現在のログオン セッションの状態オブジェクトを開き、そのオブジェクトで **IMAPIStatus::ValidateState** を呼び出した場合とまったく同じ **IXPLogon::ValidateState** 呼び出しに応答する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-142">The transport provider should respond to the **IXPLogon::ValidateState** call exactly as if the MAPI spooler had opened a status object for the current logon session and then called **IMAPIStatus::ValidateState** on that object.</span></span> 
  
<span data-ttu-id="0d3f7-143">**IMAPIStatus::ValidateState** の実装をサポートするために、MAPI スプーラーは、プロファイル セッションで実行中のすべてのアクティブなトランスポート プロバイダーのすべてのログオン オブジェクトで **IXPLogon::ValidateState** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0d3f7-143">To support its implementation of **IMAPIStatus::ValidateState**, the MAPI spooler calls **IXPLogon::ValidateState** on all logon objects for all active transport providers that are running in a profile session.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0d3f7-144">関連項目</span><span class="sxs-lookup"><span data-stu-id="0d3f7-144">See also</span></span>



[<span data-ttu-id="0d3f7-145">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="0d3f7-145">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
  
[<span data-ttu-id="0d3f7-146">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="0d3f7-146">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="0d3f7-147">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d3f7-147">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

