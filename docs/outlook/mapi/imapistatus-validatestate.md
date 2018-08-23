---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5ab459239bdcdcad30c4b6c82d5a3f8641bd4aca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567805"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="d06c0-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="d06c0-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="d06c0-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d06c0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d06c0-105">MAPI リソースまたはサービス プロバイダーの使用可能な外部のステータス情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="d06c0-106">ステータスのすべてのオブジェクトでこのメソッドがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d06c0-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="d06c0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d06c0-107">Parameters</span></span>

<span data-ttu-id="d06c0-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d06c0-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="d06c0-109">[in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="d06c0-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="d06c0-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d06c0-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d06c0-111">[in]検証を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="d06c0-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="d06c0-112">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-112">The following flags can be set:</span></span>
    
<span data-ttu-id="d06c0-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="d06c0-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="d06c0-114">ユーザー操作がキャンセルされました、通常、対応するダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="d06c0-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="d06c0-115">状態オブジェクトには、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="d06c0-116">工程の作業を続行します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="d06c0-117">操作を停止し、MAPI_E_USER_CANCELED を返します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="d06c0-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="d06c0-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="d06c0-119">1 つ以上の状態のオブジェクトの構成のプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="d06c0-120">クライアントは、動的に重要なトランスポート プロバイダーのエラーを修正するのには MAPI スプーラーを許可するには、このフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="d06c0-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="d06c0-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="d06c0-122">状態オブジェクトは、接続を実行します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-122">The status object should perform a connection.</span></span> <span data-ttu-id="d06c0-123">REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグを指定してこのフラグを使用する場合は、キャッシュを使用しない接続が発生します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="d06c0-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="d06c0-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="d06c0-125">状態オブジェクトは、切断操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="d06c0-126">REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグを指定してこのフラグを使用する場合は、キャッシュを使用しない切断が発生します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="d06c0-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="d06c0-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="d06c0-128">ヘッダー キャッシュ テーブル内のエントリを処理する必要があります、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたすべてのメッセージをダウンロードするか、および、MSGSTATUS_REMOTE_DELETE フラグでマークされたすべてのメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="d06c0-129">MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE の設定の両方を持つメッセージを移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="d06c0-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="d06c0-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="d06c0-131">リモート トランスポート プロバイダーでは、メッセージ ヘッダーの新しいリストをダウンロードする必要があり、メッセージの状態をマークするすべてのフラグをクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="d06c0-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="d06c0-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="d06c0-133">状態オブジェクトが操作の一部としてユーザー インターフェイスを表示するを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d06c0-134">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d06c0-134">Return value</span></span>

<span data-ttu-id="d06c0-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="d06c0-135">S_OK</span></span> 
  
> <span data-ttu-id="d06c0-136">検証に成功しました。</span><span class="sxs-lookup"><span data-stu-id="d06c0-136">The validation was successful.</span></span>
    
<span data-ttu-id="d06c0-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d06c0-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d06c0-138">別の操作が実行中です。完了するために許可するか、停止する、この操作を開始する前に。</span><span class="sxs-lookup"><span data-stu-id="d06c0-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="d06c0-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="d06c0-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="d06c0-140">状態オブジェクトは、検証メソッドをサポートしていません**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) のプロパティに STATUS_VALIDATE_STATE フラグがない場合で示される。</span><span class="sxs-lookup"><span data-stu-id="d06c0-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="d06c0-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d06c0-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d06c0-142">ユーザー操作がキャンセルされました検証、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。</span><span class="sxs-lookup"><span data-stu-id="d06c0-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="d06c0-143">リモート トランスポート プロバイダーによってのみ、この値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d06c0-144">注釈</span><span class="sxs-lookup"><span data-stu-id="d06c0-144">Remarks</span></span>

<span data-ttu-id="d06c0-145">**IMAPIStatus::ValidateState**メソッドは、状態オブジェクトに関連付けられているリソースの状態をチェックします。</span><span class="sxs-lookup"><span data-stu-id="d06c0-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="d06c0-146">[IMAPIStatus](imapistatusimapiprop.md)インターフェイスの状態のすべてのオブジェクトに必要な唯一の方法は、 **ValidateState**です。</span><span class="sxs-lookup"><span data-stu-id="d06c0-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="d06c0-147">このメソッドの実際の動作は実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="d06c0-148">次の表では、状態オブジェクトのさまざまな種類のそれぞれの実装について説明します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="d06c0-149">**ステータス オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="d06c0-149">**Status object**</span></span>|<span data-ttu-id="d06c0-150">* ValidateState * 実装 * *</span><span class="sxs-lookup"><span data-stu-id="d06c0-150">****ValidateState** implementation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d06c0-151">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="d06c0-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="d06c0-152">現在アクティブなサービス ・ プロバイダー、サブシステム自身が所有しているすべてのリソースの状態を検証します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="d06c0-153">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="d06c0-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="d06c0-154">ログオン用に既にログオンしているかどうかに関係なくすべてのトランスポート プロバイダーを実行します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="d06c0-155">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="d06c0-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="d06c0-156">プロファイル セクション内のエントリをチェックします。</span><span class="sxs-lookup"><span data-stu-id="d06c0-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="d06c0-157">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="d06c0-157">Service provider</span></span>  <br/> |<span data-ttu-id="d06c0-158">実装は、プロバイダーと、 _ulFlags_パラメーターで設定されているフラグの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="d06c0-159">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="d06c0-159">Notes to implementers</span></span>

<span data-ttu-id="d06c0-160">リモート クライアント アプリケーションは、リモートのさまざまなアクションの処理を開始する**ValidateState**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="d06c0-161">このメソッドは、実際に作業を行うための代わりに、MAPI スプーラーと通信するためにステータス ビットを設定するのには、主に存在します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="d06c0-162">通常、トランスポート プロバイダーは、MAPI スプーラーにクライアントの要求を完了するのには開始する必要があるアクションを示すステータス行のフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="d06c0-163">クライアント トランスポートがスプーラーの相互作用のこのモデルでは、クライアントによって要求された操作は、非同期で要求された操作が完了する前に、 **ValidateState**が返されます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="d06c0-164">ただしが必ずしも含まれず、基になるメッセージング システムまたはトランスポートに固有のインターフェイスでは、関連するアクションは、同期があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="d06c0-165">リモート トランスポート プロバイダーが実行するアクションを指定するのには、次のフラグのビットマスクで、クライアント アプリケーションに渡されます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="d06c0-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="d06c0-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="d06c0-167">可能であれば、リモート トランスポート プロバイダーでは、ヘッダーのダウンロードに関連するすべての操作を取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="d06c0-168">これを行うには、トランスポート プロバイダーは、ログオン オブジェクトの [状態] 行に次のプロパティ値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="d06c0-169">このトランスポート プロバイダーの受信のフラッシュ処理を停止するのには MAPI スプーラーに指示するのには**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) のプロパティで STATUS_INBOUND_ENABLED と STATUS_INBOUND_ACTIVE のビットをオフにします。</span><span class="sxs-lookup"><span data-stu-id="d06c0-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="d06c0-170">STATUS_OFFLINE の**PR_STATUS_CODE**プロパティ内のビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="d06c0-171">**PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) プロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="d06c0-172">ユーザーに、トランスポート プロバイダーの状態を示す文字列を**PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="d06c0-173">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="d06c0-173">Return S_OK.</span></span> <span data-ttu-id="d06c0-174">ただし、実行中の操作をキャンセルすることはできません、 **ValidateState**は MAPI_E_BUSY を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="d06c0-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="d06c0-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="d06c0-176">リモート トランスポート プロバイダーは、 [IXPLogon::FlushQueues](ixplogon-flushqueues.md)メソッドに関連する MAPI スプーラー トランスポートの操作のコンテキストの外部からの共有リソース (たとえば、モデムまたは COM ポート) への接続を確立する必要があることはありません。</span><span class="sxs-lookup"><span data-stu-id="d06c0-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="d06c0-177">**ValidateState**はこのフラグを使って呼び出されると、トランスポート プロバイダーが次の操作にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="d06c0-178">**IXPLogon::FlushQueues**メソッドが呼び出されたときに、リモート接続を確立する必要があることを示す内部フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="d06c0-179">MAPI スプーラー キュー プロセスのフラッシュを開始するのには、状態テーブルに正しい値を設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="d06c0-180">キューのフラッシュが完了すると、共有リソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="d06c0-181">STATUS_OFFLINE の**PR_STATUS_CODE**プロパティ内のビットをオフにします。</span><span class="sxs-lookup"><span data-stu-id="d06c0-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="d06c0-182">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="d06c0-182">Return S_OK.</span></span>
    
<span data-ttu-id="d06c0-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="d06c0-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="d06c0-184">リモート トランスポート プロバイダーは、メッセージング システムのリソースへの接続を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="d06c0-185">その後で、 **PR_STATUS_CODE**プロパティに STATUS_OFFLINE ビットを設定する必要があります、S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="d06c0-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="d06c0-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="d06c0-187">リモート トランスポート プロバイダーは、必要がありますリモートのメッセージを処理し、保留されているすべてのメッセージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="d06c0-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="d06c0-188">これを行うには、トランスポート プロバイダーは、ログオン オブジェクトの [状態] 行に次のプロパティ値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="d06c0-189">ユーザーに、トランスポート プロバイダーの状態を示す文字列を**PR_STATUS_STRING**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="d06c0-190">[ **PR_STATUS_CODE** ] プロパティには、STATUS_OUTBOUND_ENABLED と STATUS_OUTBOUND_ACTIVE のビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="d06c0-191">False を指定するトランスポート プロバイダーの状態の行の**PR_REMOTE_VALIDATE_OK**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="d06c0-192">(ヘッダーをダウンロードするには) などの進行中の別の操作の場合**ValidateState**が呼び出されると、 **ValidateState**は MAPI_E_BUSY を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="d06c0-193">Microsoft Exchange クライアントの要件を満たすために、同様に、REFRESH_XP_HEADER_CACHE フラグを処理するためのコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="d06c0-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="d06c0-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="d06c0-195">リモート トランスポート プロバイダーは、メッセージング システムから新しいメッセージ ヘッダーを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="d06c0-196">これを行うには、トランスポート プロバイダーは次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="d06c0-197">ユーザーに、トランスポート プロバイダーの状態を示す文字列を**PR_STATUS_STRING**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="d06c0-198">[ **PR_STATUS_CODE** ] プロパティには、STATUS_INBOUND_ENABLED と STATUS_INBOUND_ACTIVE のビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="d06c0-199">STATUS_OFFLINE の**PR_STATUS_CODE**プロパティ内のビットをオフにします。</span><span class="sxs-lookup"><span data-stu-id="d06c0-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="d06c0-200">STATUS_ONLINE の**PR_STATUS_CODE**プロパティ内のビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="d06c0-201">False を指定するトランスポート プロバイダーの状態の行の**PR_REMOTE_VALIDATE_OK**プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="d06c0-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="d06c0-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="d06c0-203">トランスポート プロバイダーは、メッセージのダウンロードを確認するダイアログ ボックス) など、メッセージのヘッダーを処理するためのユーザー インターフェイスの任意の部分には、そのダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="d06c0-204">それ以外の場合、 **ValidateState**は、MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="d06c0-205">これら以外のすべてのフラグが渡されると、 **ValidateState**は MAPI_E_UNKNOWN_FLAGS を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="d06c0-206">トランスポート プロバイダーは、クライアントの呼び出しは、 **IMAPIStatus::ValidateState**メソッドになります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="d06c0-207">**ValidateState**の処理中にトランスポート プロバイダーは、モデムまたは COM ポートなど、限られたシステム リソースの割り当てすべてのアクションを行わないでください。</span><span class="sxs-lookup"><span data-stu-id="d06c0-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="d06c0-208">これは、MAPI スプーラーは、トランスポート プロバイダーを 1 つ以上のキューをフラッシュする必要がありますので。</span><span class="sxs-lookup"><span data-stu-id="d06c0-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="d06c0-209">ただし、クライアントは、いつでも任意のトランスポート プロバイダーの**ValidateState**メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="d06c0-210">トランスポート プロバイダーは、 **ValidateState**の処理中に貴重なリソースを割り当てるしようとする場合、エラーは発生する MAPI スプーラーのキューをフラッシュするように指示する別のトランスポート プロバイダーとの競合が発生したためです。</span><span class="sxs-lookup"><span data-stu-id="d06c0-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="d06c0-211">MAPI スプーラーの指示の下で発生するすべての貴重なリソースの割り当てを許可する場合は、このような競合を回避できます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="d06c0-212">トランスポート プロバイダーは、クライアント アプリケーションは、トランスポート プロバイダーは、ビジー状態または待機操作を実行するのには、MAPI スプーラーを無効にするときを検出できるように**PR_REMOTE_VALIDATE_OK**プロパティをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d06c0-213">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d06c0-213">Notes to callers</span></span>

<span data-ttu-id="d06c0-214">なる可能性がある時間のかかる他の呼び出しはこのメソッドが原因で発生するため、 **ValidateState**は、このメソッドが別の操作が完了するの待っていることを通知するために MAPI_E_BUSY を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="d06c0-215">別のタスクを実行する前に保留中の操作が完了するまでを待機する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="d06c0-216">プロバイダーの状態のオブジェクトを転送するのには、呼び出しを細かく制御があります。</span><span class="sxs-lookup"><span data-stu-id="d06c0-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="d06c0-217">**ValidateState**トランスポート プロバイダーの操作に影響を与えるには、1 つまたは複数のフラグを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="d06c0-218">たとえば、ABORT_XP_HEADER_OPERATION フラグは、ユーザーが検証をキャンセルすることを示します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="d06c0-219">トランスポート プロバイダーは、MAPI_E_USER_CANCELED を返すことを中止するには決定できますか、続けることができます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="d06c0-220">構成オプションが変更されたことを示すためにサービス ・ プロバイダーの状態オブジェクト、または MAPI スプーラーへの呼び出しには、CONFIG_CHANGED フラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="d06c0-221">トランスポート プロバイダーを動的に再構成するのに CONFIG_CHANGED を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="d06c0-222">サービス プロバイダーの状態のオブジェクトへの呼び出しに CONFIG_CHANGED を設定すると、プロバイダーは、MAPI スプーラーを無効に変更を通知する[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)への呼び出しに応答します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="d06c0-223">MAPI スプーラーを無効の状態のオブジェクトへの呼び出しに CONFIG_CHANGED を設定すると、スプーラーは、アクティブなトランスポート プロバイダーごとに[IXPLogon::AddressTypes](ixplogon-addresstypes.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="d06c0-224">**AddressTypes**は、トランスポートのサポートされているアドレスの種類の MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="d06c0-225">サービス プロバイダーによっては、検証の時間がかかるが予想される場合にも、進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="d06c0-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="d06c0-226">進行状況のインジケーターを表示するが役に立つ、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="d06c0-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="d06c0-227">SUPPRESS_UI フラグを設定すると、プロパティ シートの構成や進行状況ダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="d06c0-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d06c0-228">関連項目</span><span class="sxs-lookup"><span data-stu-id="d06c0-228">See also</span></span>

- [<span data-ttu-id="d06c0-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="d06c0-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="d06c0-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="d06c0-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="d06c0-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="d06c0-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="d06c0-232">PidTagRemoteValidateOk 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d06c0-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="d06c0-233">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d06c0-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="d06c0-234">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d06c0-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="d06c0-235">PidTagStatusString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="d06c0-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="d06c0-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d06c0-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

