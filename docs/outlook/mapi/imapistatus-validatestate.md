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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438149"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="0757c-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="0757c-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="0757c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0757c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0757c-105">MAPI リソースまたはサービス プロバイダーで使用可能な外部状態情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="0757c-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="0757c-106">このメソッドは、すべての状態オブジェクトでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0757c-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0757c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0757c-107">Parameters</span></span>

<span data-ttu-id="0757c-108">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0757c-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="0757c-109">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0757c-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="0757c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0757c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="0757c-111">[in]検証を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0757c-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="0757c-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0757c-112">The following flags can be set:</span></span>
    
<span data-ttu-id="0757c-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="0757c-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="0757c-114">ユーザーは、通常、対応するダイアログ ボックスの [ **キャンセル** ] ボタンをクリックして、操作をキャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="0757c-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="0757c-115">status オブジェクトには、次の 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="0757c-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="0757c-116">操作の作業を続行します。</span><span class="sxs-lookup"><span data-stu-id="0757c-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="0757c-117">操作を停止し、操作をMAPI_E_USER_CANCELED。</span><span class="sxs-lookup"><span data-stu-id="0757c-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="0757c-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="0757c-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="0757c-119">1 つ以上の状態オブジェクトの構成プロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="0757c-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="0757c-120">クライアントは、MAPI スプーラーが重大なトランスポート プロバイダーのエラーを動的に修正できるよう、このフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0757c-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="0757c-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="0757c-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="0757c-122">status オブジェクトは接続を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-122">The status object should perform a connection.</span></span> <span data-ttu-id="0757c-123">このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHEと一緒に使用すると、接続はキャッシュなしで行われます。</span><span class="sxs-lookup"><span data-stu-id="0757c-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="0757c-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="0757c-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="0757c-125">status オブジェクトは切断操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="0757c-126">このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHEと一緒に使用すると、切断はキャッシュなしで行われます。</span><span class="sxs-lookup"><span data-stu-id="0757c-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="0757c-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="0757c-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="0757c-128">ヘッダー キャッシュ テーブル内のエントリを処理し、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたメッセージはすべてダウンロードし、MSGSTATUS_REMOTE_DELETE フラグでマークされたメッセージはすべて削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="0757c-129">設定されたメッセージとMSGSTATUS_REMOTE_DOWNLOAD設定MSGSTATUS_REMOTE_DELETEメッセージを移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="0757c-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="0757c-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="0757c-131">リモート トランスポート プロバイダーの場合は、メッセージ ヘッダーの新しい一覧をダウンロードし、メッセージの状態を示すフラグはすべてクリアする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="0757c-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="0757c-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="0757c-133">status オブジェクトが操作の一部としてユーザー インターフェイスを表示しなかします。</span><span class="sxs-lookup"><span data-stu-id="0757c-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0757c-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="0757c-134">Return value</span></span>

<span data-ttu-id="0757c-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="0757c-135">S_OK</span></span> 
  
> <span data-ttu-id="0757c-136">検証が成功しました。</span><span class="sxs-lookup"><span data-stu-id="0757c-136">The validation was successful.</span></span>
    
<span data-ttu-id="0757c-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="0757c-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="0757c-138">別の操作が進行中です。この操作を開始する前に、完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="0757c-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="0757c-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="0757c-140">**status** オブジェクトは、PR_RESOURCE_METHODS ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_VALIDATE_STATE フラグがない場合に示される検証メソッドをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="0757c-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="0757c-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0757c-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0757c-142">ユーザーは、通常、ダイアログ ボックスの [キャンセル]ボタンをクリックして、検証操作をキャンセルしました。</span><span class="sxs-lookup"><span data-stu-id="0757c-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="0757c-143">この値は、リモート トランスポート プロバイダーによってのみ返されます。</span><span class="sxs-lookup"><span data-stu-id="0757c-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0757c-144">注釈</span><span class="sxs-lookup"><span data-stu-id="0757c-144">Remarks</span></span>

<span data-ttu-id="0757c-145">**IMAPIStatus::ValidateState** メソッドは、状態オブジェクトに関連付けられているリソースの状態をチェックします。</span><span class="sxs-lookup"><span data-stu-id="0757c-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="0757c-146">**ValidateState** は、すべての状態オブジェクトに必要な [IMAPIStatus](imapistatusimapiprop.md) インターフェイス内の唯一のメソッドです。</span><span class="sxs-lookup"><span data-stu-id="0757c-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="0757c-147">このメソッドの正確な動作は、実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="0757c-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="0757c-148">次の表では、さまざまな種類の状態オブジェクトの実装について説明します。</span><span class="sxs-lookup"><span data-stu-id="0757c-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="0757c-149">**Status オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="0757c-149">**Status object**</span></span>|<span data-ttu-id="0757c-150">ValidateState\*\* の実装\*\*</span><span class="sxs-lookup"><span data-stu-id="0757c-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="0757c-151">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="0757c-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="0757c-152">現在アクティブなサービス プロバイダーとサブシステム自体が所有しているすべてのリソースの状態を検証します。</span><span class="sxs-lookup"><span data-stu-id="0757c-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="0757c-153">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="0757c-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="0757c-154">既にログオンしているかどうかに関係なく、すべてのトランスポート プロバイダーのログオンを実行します。</span><span class="sxs-lookup"><span data-stu-id="0757c-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="0757c-155">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="0757c-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="0757c-156">プロファイル セクションのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="0757c-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="0757c-157">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0757c-157">Service provider</span></span>  <br/> |<span data-ttu-id="0757c-158">実装は、プロバイダーの種類と  _ulFlags パラメーターで設定されたフラグによって異_ なります。</span><span class="sxs-lookup"><span data-stu-id="0757c-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="0757c-159">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="0757c-159">Notes to implementers</span></span>

<span data-ttu-id="0757c-160">リモート クライアント アプリケーションは ValidateState メソッドを **呼び出** して、さまざまなアクションのリモート処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="0757c-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="0757c-161">このメソッドは主に、MAPI スプーラーと通信するための状態ビットを設定するために存在します。実際に作業を行う代わりに。</span><span class="sxs-lookup"><span data-stu-id="0757c-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="0757c-162">通常、トランスポート プロバイダーは、クライアントの要求を完了するために開始する必要があるアクションを MAPI スプーラーに示すフラグを状態行に設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="0757c-163">このクライアント トランスポート スプーラー操作のモデルでは、要求されたアクションが完了する前に **ValidateState** が返されるという、クライアントによって要求されたアクションは非同期です。</span><span class="sxs-lookup"><span data-stu-id="0757c-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="0757c-164">ただし、基になるメッセージング システムを必ずしも必要としないアクション、またはトランスポート固有のインターフェイスを含むアクションは同期可能です。</span><span class="sxs-lookup"><span data-stu-id="0757c-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="0757c-165">クライアント アプリケーションは、次のフラグのビットマスクを渡して、リモート トランスポート プロバイダーが実行するアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="0757c-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="0757c-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="0757c-167">可能であれば、リモート トランスポート プロバイダーは、ヘッダーのダウンロードに関連する操作を取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="0757c-168">これを行うには、トランスポート プロバイダーはログオン オブジェクトの状態行に次のプロパティ値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="0757c-169">PR_STATUS_CODE ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの **STATUS_INBOUND_ENABLED** ビットと STATUS_INBOUND_ACTIVE ビットをクリアして、このトランスポート プロバイダーの受信フラッシュ プロセスを停止する MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="0757c-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="0757c-170">プロパティでSTATUS_OFFLINEビットを **PR_STATUS_CODE** します。</span><span class="sxs-lookup"><span data-stu-id="0757c-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="0757c-171">[プロパティ] **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) プロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="0757c-172">ユーザーに **PR_STATUS_STRING** を示す文字列にプロパティ [(PidTagStatusString)](pidtagstatusstring-canonical-property.md)プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="0757c-173">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="0757c-173">Return S_OK.</span></span> <span data-ttu-id="0757c-174">ただし、進行中の操作を取り消しできない場合は **、ValidateState** はデータをMAPI_E_BUSY。</span><span class="sxs-lookup"><span data-stu-id="0757c-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="0757c-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="0757c-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="0757c-176">リモート トランスポート プロバイダーは [、IXPLogon::FlushQueues](ixplogon-flushqueues.md) メソッドに関係する MAPI スプーラー トランスポートの相互作用のコンテキスト外で共有リソース (モデムや COM ポートなど) への接続を確立しなけれ。</span><span class="sxs-lookup"><span data-stu-id="0757c-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="0757c-177">ValidateState **をこの** フラグで呼び出す場合、トランスポート プロバイダーは次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="0757c-178">**IXPLogon::FlushQueues** メソッドの呼び出し時にリモート接続を確立する必要がある場合は、内部状態フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="0757c-179">MAPI スプーラーがキューのフラッシュ プロセスを開始する状態テーブルの正しい値を設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="0757c-180">キューのフラッシュが完了したら、共有リソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="0757c-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="0757c-181">プロパティのSTATUS_OFFLINEビットを **PR_STATUS_CODE** します。</span><span class="sxs-lookup"><span data-stu-id="0757c-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="0757c-182">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="0757c-182">Return S_OK.</span></span>
    
<span data-ttu-id="0757c-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="0757c-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="0757c-184">リモート トランスポート プロバイダーは、メッセージング システム リソースへの接続を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="0757c-185">これを行った後、STATUS_OFFLINE プロパティで STATUS_OFFLINE ビットを設定し、PR_STATUS_CODEを返S_OK。</span><span class="sxs-lookup"><span data-stu-id="0757c-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="0757c-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="0757c-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="0757c-187">リモート トランスポート プロバイダーは、リモート メッセージを処理し、延期されたメッセージをアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="0757c-188">これを行うには、トランスポート プロバイダーはログオン オブジェクトの状態行に次のプロパティ値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="0757c-189">トランスポート プロバイダー **PR_STATUS_STRING** をユーザーに示す文字列に、PR_STATUS_STRING プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="0757c-190">プロパティでSTATUS_OUTBOUND_ENABLEDビットSTATUS_OUTBOUND_ACTIVEビットを **PR_STATUS_CODE** します。</span><span class="sxs-lookup"><span data-stu-id="0757c-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="0757c-191">トランスポート プロバイダー **のPR_REMOTE_VALIDATE_OK** のプロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="0757c-192">**ValidateState** が呼び出された場合に別の操作 (ヘッダーのダウンロードなど) が進行中の場合は **、ValidateState** はヘッダーを返MAPI_E_BUSY。</span><span class="sxs-lookup"><span data-stu-id="0757c-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="0757c-193">Microsoft クライアントの要件を満たすために、REFRESH_XP_HEADER_CACHE フラグを処理するコードExchangeします。</span><span class="sxs-lookup"><span data-stu-id="0757c-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="0757c-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="0757c-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="0757c-195">リモート トランスポート プロバイダーは、メッセージング システムから新しいメッセージ ヘッダーを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="0757c-196">これを行うには、トランスポート プロバイダーは次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="0757c-197">トランスポート プロバイダー **PR_STATUS_STRING** をユーザーに示す文字列に、PR_STATUS_STRING プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="0757c-198">プロパティでSTATUS_INBOUND_ENABLEDビットSTATUS_INBOUND_ACTIVEビットを **設定** PR_STATUS_CODEします。</span><span class="sxs-lookup"><span data-stu-id="0757c-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="0757c-199">プロパティのSTATUS_OFFLINEビットを **PR_STATUS_CODE** します。</span><span class="sxs-lookup"><span data-stu-id="0757c-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="0757c-200">プロパティでSTATUS_ONLINEビットを **PR_STATUS_CODE** します。</span><span class="sxs-lookup"><span data-stu-id="0757c-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="0757c-201">トランスポート プロバイダー **のPR_REMOTE_VALIDATE_OK** のプロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="0757c-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="0757c-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="0757c-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="0757c-203">トランスポート プロバイダーにメッセージ ヘッダーを処理するためのユーザー インターフェイス (メッセージのダウンロードを確認するダイアログ ボックスなど) がある場合は、そのダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0757c-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="0757c-204">それ以外の場合 **、ValidateState** は、MAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="0757c-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="0757c-205">これらのフラグ以外のフラグが渡された場合は **、ValidateState** は値を返MAPI_E_UNKNOWN_FLAGS。</span><span class="sxs-lookup"><span data-stu-id="0757c-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="0757c-206">トランスポート プロバイダーへのクライアントの呼び出しは、多くの場合 **、IMAPIStatus::ValidateState メソッドに対して行** います。</span><span class="sxs-lookup"><span data-stu-id="0757c-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="0757c-207">**ValidateState** の処理中に、トランスポート プロバイダーは、モデムや COM ポートなど、不足しているシステム リソースを割り当てるアクションを実行しなけい。</span><span class="sxs-lookup"><span data-stu-id="0757c-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="0757c-208">これは、MAPI スプーラーが複数のトランスポート プロバイダーでキューをフラッシュする必要がある場合があるためです。</span><span class="sxs-lookup"><span data-stu-id="0757c-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="0757c-209">ただし、クライアントは、任意のトランスポート プロバイダーの **ValidateState** メソッドをいつでも呼び出できます。</span><span class="sxs-lookup"><span data-stu-id="0757c-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="0757c-210">**ValidateState** の処理中にトランスポート プロバイダーが不足しているリソースを割り当てしようとすると、MAPI スプーラーがキューをフラッシュするように指示した別のトランスポート プロバイダーとの競合が原因でエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="0757c-211">MAPI スプーラーの指示に従って、すべての不足しているリソース割り当てを許可する場合は、このような競合を回避できます。</span><span class="sxs-lookup"><span data-stu-id="0757c-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="0757c-212">トランスポート プロバイダーは、トランスポート **プロバイダーがビジー状態または** MAPI スプーラーがアクションを開始するのを待っているときにクライアント アプリケーションが検出できるよう、PR_REMOTE_VALIDATE_OK プロパティをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0757c-213">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0757c-213">Notes to callers</span></span>

<span data-ttu-id="0757c-214">このメソッドは、他の潜在的に長い呼び出しを行う原因となる可能性があるため **、ValidateState** は MAPI_E_BUSY を返して、このメソッドが別の操作の完了を待機しているという通知を受け取る場合があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="0757c-215">別のタスクを試みる前に、保留中の操作が完了するまで待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="0757c-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="0757c-216">トランスポート プロバイダーの状態オブジェクトへの呼び出しを最も制御できます。</span><span class="sxs-lookup"><span data-stu-id="0757c-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="0757c-217">1 つ以上のフラグを **ValidateState** に渡して、トランスポート プロバイダーの操作に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="0757c-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="0757c-218">たとえば、ABORT_XP_HEADER_OPERATIONフラグは、ユーザーが検証を取り消したと示します。</span><span class="sxs-lookup"><span data-stu-id="0757c-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="0757c-219">トランスポート プロバイダーは、中止、返す、または続行MAPI_E_USER_CANCELED決定できます。</span><span class="sxs-lookup"><span data-stu-id="0757c-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="0757c-220">呼び出しの CONFIG_CHANGEDフラグをサービス プロバイダーの status オブジェクトまたは MAPI スプーラーに設定して、構成オプションが変更されたかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0757c-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="0757c-221">トランスポート プロバイダーを動的CONFIG_CHANGED再構成するには、次の情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="0757c-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="0757c-222">サービス プロバイダーの状態オブジェクトへの呼び出しで CONFIG_CHANGED を設定すると、プロバイダーは [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) への呼び出しで応答し、MAPI スプーラーに変更を通知します。</span><span class="sxs-lookup"><span data-stu-id="0757c-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="0757c-223">MAPI スプーラー CONFIG_CHANGED呼び出し時に、スプーラーはアクティブなトランスポート プロバイダーごとに [IXPLogon::AddressTypes](ixplogon-addresstypes.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0757c-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="0757c-224">**AddressTypes は** 、トランスポートでサポートされているアドレスの種類を MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="0757c-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="0757c-225">一部のサービス プロバイダーは、検証に時間がかかると予想される場合は進行状況インジケーターも表示します。</span><span class="sxs-lookup"><span data-stu-id="0757c-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="0757c-226">進行状況インジケーターの表示は役に立ちますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="0757c-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="0757c-227">このフラグSUPPRESS_UI設定すると、構成プロパティ シートや進行状況ダイアログ ボックスを表示できません。</span><span class="sxs-lookup"><span data-stu-id="0757c-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0757c-228">関連項目</span><span class="sxs-lookup"><span data-stu-id="0757c-228">See also</span></span>

- [<span data-ttu-id="0757c-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="0757c-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="0757c-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="0757c-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="0757c-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="0757c-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="0757c-232">PidTagRemoteValidateOk 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0757c-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="0757c-233">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0757c-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="0757c-234">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0757c-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="0757c-235">PidTagStatusString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0757c-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="0757c-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0757c-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

