---
title: imapistatusvalidatestate
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
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331550"
---
# <a name="imapistatusvalidatestate"></a><span data-ttu-id="1fbc3-103">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="1fbc3-103">IMAPIStatus::ValidateState</span></span>

<span data-ttu-id="1fbc3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1fbc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1fbc3-105">MAPI リソースまたはサービスプロバイダーに対して使用可能な外部状態情報を確認します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-105">Confirms the external status information available for the MAPI resource or the service provider.</span></span> <span data-ttu-id="1fbc3-106">このメソッドは、すべての status オブジェクトでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-106">This method is supported in all status objects.</span></span> 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1fbc3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1fbc3-107">Parameters</span></span>

<span data-ttu-id="1fbc3-108">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="1fbc3-108">_ulUIParam_</span></span>
  
> <span data-ttu-id="1fbc3-109">順番このメソッドが表示するダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-109">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
<span data-ttu-id="1fbc3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1fbc3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1fbc3-111">順番検証を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-111">[in] A bitmask of flags that controls the validation.</span></span> <span data-ttu-id="1fbc3-112">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-112">The following flags can be set:</span></span>
    
<span data-ttu-id="1fbc3-113">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="1fbc3-113">ABORT_XP_HEADER_OPERATION</span></span>
  
> <span data-ttu-id="1fbc3-114">ユーザーが操作をキャンセルしました。通常は、対応するダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-114">The user canceled the operation, typically by clicking the **Cancel** button in the corresponding dialog box.</span></span> <span data-ttu-id="1fbc3-115">status オブジェクトには、次の2つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-115">The status object has two options:</span></span> 
    
   - <span data-ttu-id="1fbc3-116">操作を続行します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-116">Continue working on the operation.</span></span>
    
   - <span data-ttu-id="1fbc3-117">操作を停止し、MAPI_E_USER_CANCELED を返します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-117">Stop the operation and return MAPI_E_USER_CANCELED.</span></span>
    
<span data-ttu-id="1fbc3-118">CONFIG_CHANGED</span><span class="sxs-lookup"><span data-stu-id="1fbc3-118">CONFIG_CHANGED</span></span> 
  
> <span data-ttu-id="1fbc3-119">1つ以上の状態オブジェクトの構成プロパティが変更されました。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-119">One or more of the status object's configuration properties changed.</span></span> <span data-ttu-id="1fbc3-120">クライアントはこのフラグを設定して、MAPI スプーラーが重要なトランスポートプロバイダーのエラーを動的に修正できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-120">Clients can set this flag to allow the MAPI spooler to dynamically correct critical transport provider failures.</span></span> 
    
<span data-ttu-id="1fbc3-121">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="1fbc3-121">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="1fbc3-122">status オブジェクトは、接続を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-122">The status object should perform a connection.</span></span> <span data-ttu-id="1fbc3-123">このフラグを REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグと共に使用すると、接続はキャッシュなしで行われます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-123">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the connection occurs without caching.</span></span>
    
<span data-ttu-id="1fbc3-124">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="1fbc3-124">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="1fbc3-125">status オブジェクトは、切断操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-125">The status object should perform a disconnect operation.</span></span> <span data-ttu-id="1fbc3-126">このフラグが REFRESH_XP_HEADER_CACHE または PROCESS_XP_HEADER_CACHE フラグと共に使用されている場合、切断はキャッシュなしで行われます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-126">When this flag is used with the REFRESH_XP_HEADER_CACHE or PROCESS_XP_HEADER_CACHE flag, the disconnection occurs without caching.</span></span>
    
<span data-ttu-id="1fbc3-127">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="1fbc3-127">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="1fbc3-128">ヘッダーキャッシュテーブル内のエントリを処理する必要があり、MSGSTATUS_REMOTE_DOWNLOAD フラグでマークされたすべてのメッセージをダウンロードして、MSGSTATUS_REMOTE_DELETE フラグでマークされたすべてのメッセージを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-128">Entries in the header cache table should be processed, all messages marked with the MSGSTATUS_REMOTE_DOWNLOAD flag should be downloaded, and all messages marked with the MSGSTATUS_REMOTE_DELETE flag should be deleted.</span></span> <span data-ttu-id="1fbc3-129">MSGSTATUS_REMOTE_DOWNLOAD と MSGSTATUS_REMOTE_DELETE の両方が設定されたメッセージは移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-129">Messages that have both MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE set should be moved.</span></span>
    
<span data-ttu-id="1fbc3-130">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="1fbc3-130">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="1fbc3-131">リモートトランスポートプロバイダーの場合は、メッセージヘッダーの新しいリストがダウンロードされ、メッセージの状態をマークするすべてのフラグがクリアされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-131">For a remote transport provider, a new list of message headers should be downloaded and all flags that mark message status should be cleared.</span></span>
    
<span data-ttu-id="1fbc3-132">SUPPRESS_UI</span><span class="sxs-lookup"><span data-stu-id="1fbc3-132">SUPPRESS_UI</span></span> 
  
> <span data-ttu-id="1fbc3-133">status オブジェクトが操作の一部としてユーザーインターフェイスを表示できないようにします。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-133">Prevents the status object from displaying a user interface as part of the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1fbc3-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="1fbc3-134">Return value</span></span>

<span data-ttu-id="1fbc3-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="1fbc3-135">S_OK</span></span> 
  
> <span data-ttu-id="1fbc3-136">検証に成功しました。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-136">The validation was successful.</span></span>
    
<span data-ttu-id="1fbc3-137">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1fbc3-137">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1fbc3-138">別の操作が進行中です。この操作を開始する前に、これを完了させるか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-138">Another operation is in progress; it should be allowed to complete, or it should be stopped, before this operation is initiated.</span></span>
    
<span data-ttu-id="1fbc3-139">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1fbc3-139">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1fbc3-140">status オブジェクトは、 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティの STATUS_VALIDATE_STATE フラグが指定されていない場合に、検証方法をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-140">The status object does not support the validation method, as indicated by the absence of the STATUS_VALIDATE_STATE flag in the **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="1fbc3-141">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1fbc3-141">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1fbc3-142">ユーザーが検証操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-142">The user canceled the validation operation, typically by clicking the **Cancel** button in a dialog box.</span></span> <span data-ttu-id="1fbc3-143">この値は、リモートトランスポートプロバイダーによってのみ返されます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-143">This value is returned only by remote transport providers.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1fbc3-144">解説</span><span class="sxs-lookup"><span data-stu-id="1fbc3-144">Remarks</span></span>

<span data-ttu-id="1fbc3-145">**imapistatus:: validatestate**メソッドは、status オブジェクトに関連付けられているリソースの状態をチェックします。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-145">The **IMAPIStatus::ValidateState** method checks the state of a resource that is associated with a status object.</span></span> <span data-ttu-id="1fbc3-146">**validatestate**は、すべての状態オブジェクトに必要な[imapistatus](imapistatusimapiprop.md)インターフェイスの唯一のメソッドです。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-146">**ValidateState** is the only method in the [IMAPIStatus](imapistatusimapiprop.md) interface that is required for all status objects.</span></span> <span data-ttu-id="1fbc3-147">このメソッドの正確な動作は、実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-147">The exact behavior of this method depends on the implementation.</span></span> <span data-ttu-id="1fbc3-148">次の表では、さまざまな種類の状態オブジェクトの実装について説明します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-148">The following table describes the implementation of each of the different types of status objects.</span></span> 
  
|<span data-ttu-id="1fbc3-149">**Status オブジェクト**</span><span class="sxs-lookup"><span data-stu-id="1fbc3-149">**Status object**</span></span>|<span data-ttu-id="1fbc3-150">validatestate \* \* 実装 \* \*</span><span class="sxs-lookup"><span data-stu-id="1fbc3-150">\*\*\*\*ValidateState\*\* implementation\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fbc3-151">MAPI サブシステム</span><span class="sxs-lookup"><span data-stu-id="1fbc3-151">MAPI subsystem</span></span>  <br/> |<span data-ttu-id="1fbc3-152">現在アクティブなサービスプロバイダとサブシステム自体が所有しているすべてのリソースの状態を検証します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-152">Validates the state of all the resources that the currently active service providers and the subsystem itself own.</span></span>  <br/> |
|<span data-ttu-id="1fbc3-153">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="1fbc3-153">MAPI spooler</span></span>  <br/> |<span data-ttu-id="1fbc3-154">既にログオンしているかどうかにかかわらず、すべてのトランスポートプロバイダーのログオンを実行します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-154">Performs a logon of all transport providers, regardless of whether they are already logged on.</span></span>  <br/> |
|<span data-ttu-id="1fbc3-155">MAPI アドレス帳</span><span class="sxs-lookup"><span data-stu-id="1fbc3-155">MAPI address book</span></span>  <br/> |<span data-ttu-id="1fbc3-156">[プロファイル] セクションのエントリを確認します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-156">Checks the entries in its profile section.</span></span>  <br/> |
|<span data-ttu-id="1fbc3-157">サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="1fbc3-157">Service provider</span></span>  <br/> |<span data-ttu-id="1fbc3-158">実装は、プロバイダーの種類と_ulflags_パラメーターで設定されたフラグによって異なります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-158">Implementation depends on the type of provider and the flags set in the  _ulFlags_ parameter.</span></span>  <br/> |
   
## <a name="notes-to-implementers"></a><span data-ttu-id="1fbc3-159">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="1fbc3-159">Notes to implementers</span></span>

<span data-ttu-id="1fbc3-160">リモートクライアントアプリケーションは、 **validatestate**メソッドを呼び出して、さまざまなアクションのリモート処理を開始します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-160">Remote client applications call the **ValidateState** method to start remote processing for various actions.</span></span> <span data-ttu-id="1fbc3-161">このメソッドは、主に、実際に作業を行うのではなく、MAPI スプーラーと通信するようにステータスビットを設定することによって発生します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-161">This method exists primarily to set status bits to communicate with the MAPI spooler, instead of to actually do any work.</span></span> <span data-ttu-id="1fbc3-162">通常、トランスポートプロバイダーは、MAPI スプーラーに対して、クライアントの要求を完了するために開始する必要のあるアクションを示す状態行にフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-162">Typically, the transport provider sets flags in its status row that indicate to the MAPI spooler what actions need to be initiated to complete the client's request.</span></span> 

<span data-ttu-id="1fbc3-163">このクライアントトランスポートスプーラー相互作用モデルでは、クライアントによって要求されたアクションは、要求された操作が完了する前にその**validatestate**が戻ることによって返されます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-163">In this model of client-transport-spooler interaction, the actions requested by the client are asynchronous, in that **ValidateState** returns before the requested actions are complete.</span></span> <span data-ttu-id="1fbc3-164">ただし、基になるメッセージングシステムを必要としないアクションや、トランスポート固有のインターフェイスを必要とするアクションは、同期することができます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-164">However, actions that do not necessarily involve the underlying messaging system, or that involve a transport-specific interface, can be synchronous.</span></span> <span data-ttu-id="1fbc3-165">クライアントアプリケーションは、リモートトランスポートプロバイダーが実行するアクションを指定するために、次のフラグのビットマスクを渡します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-165">The client application passes in a bitmask of the following flags to specify which actions the remote transport provider should take.</span></span> 
  
<span data-ttu-id="1fbc3-166">ABORT_XP_HEADER_OPERATION</span><span class="sxs-lookup"><span data-stu-id="1fbc3-166">ABORT_XP_HEADER_OPERATION</span></span> 
  
> <span data-ttu-id="1fbc3-167">可能であれば、リモートトランスポートプロバイダーは、ヘッダーのダウンロードに関連する操作をすべて取り消す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-167">If possible, the remote transport provider should cancel any operations that involve downloading headers.</span></span> <span data-ttu-id="1fbc3-168">これを行うには、トランスポートプロバイダーは、ログオンオブジェクトの状態の行に次のプロパティ値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-168">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="1fbc3-169">**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの STATUS_INBOUND_ENABLED および STATUS_INBOUND_ACTIVE ビットをクリアして、このトランスポートプロバイダーの着信フラッシュプロセスを停止するように MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-169">Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to halt the incoming flush process for this transport provider.</span></span>
    
   - <span data-ttu-id="1fbc3-170">**PR_STATUS_CODE**プロパティの STATUS_OFFLINE ビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-170">Set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="1fbc3-171">**PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) プロパティを TRUE に設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-171">Set the **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) property to TRUE.</span></span>
    
   - <span data-ttu-id="1fbc3-172">**PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) プロパティを、トランスポートプロバイダーのユーザーに対する状態を示す文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-172">Set the **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) property to a string that indicates the transport provider's status to the user.</span></span>
    
   - <span data-ttu-id="1fbc3-173">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="1fbc3-173">Return S_OK.</span></span> <span data-ttu-id="1fbc3-174">ただし、処理中の操作を取り消すことができない場合、 **validatestate**は MAPI_E_BUSY を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-174">However, if the operation in progress cannot be canceled, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
<span data-ttu-id="1fbc3-175">FORCE_XP_CONNECT</span><span class="sxs-lookup"><span data-stu-id="1fbc3-175">FORCE_XP_CONNECT</span></span> 
  
> <span data-ttu-id="1fbc3-176">リモートトランスポートプロバイダーは、 [IXPLogon:: flushqueues](ixplogon-flushqueues.md)メソッドに含まれる MAPI スプーラートランスポート相互作用のコンテキストの外部にある共有リソース (モデム、COM ポートなど) への接続を確立することはできません。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-176">A remote transport provider should never establish a connection to a shared resource (for example, a modem or COM port) outside the context of the MAPI spooler-transport interaction involved in the [IXPLogon::FlushQueues](ixplogon-flushqueues.md) method.</span></span> <span data-ttu-id="1fbc3-177">このフラグを使用して**validatestate**を呼び出す場合、トランスポートプロバイダーは次の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-177">If **ValidateState** is called with this flag, your transport provider should do the following:</span></span> 
    
   - <span data-ttu-id="1fbc3-178">**IXPLogon:: flushqueues**メソッドが呼び出されたときにリモート接続を確立する必要があることを示す内部状態フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-178">Set an internal status flag to indicate that the remote connection must be established when the **IXPLogon::FlushQueues** method is called.</span></span> 
    
   - <span data-ttu-id="1fbc3-179">状態テーブルの正しい値を設定して、MAPI スプーラーがキューのフラッシュプロセスを開始するようにします。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-179">Set the correct values in the status table to cause the MAPI spooler to initiate the queue flushing process.</span></span>
    
   - <span data-ttu-id="1fbc3-180">キューのフラッシュが完了したら、共有リソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-180">When flushing of queues is complete, release the shared resource.</span></span>
    
   - <span data-ttu-id="1fbc3-181">**PR_STATUS_CODE**プロパティの STATUS_OFFLINE ビットをオフにします。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-181">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="1fbc3-182">S_OK ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="1fbc3-182">Return S_OK.</span></span>
    
<span data-ttu-id="1fbc3-183">FORCE_XP_DISCONNECT</span><span class="sxs-lookup"><span data-stu-id="1fbc3-183">FORCE_XP_DISCONNECT</span></span> 
  
> <span data-ttu-id="1fbc3-184">リモートトランスポートプロバイダーは、メッセージングシステムのリソースへの接続を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-184">The remote transport provider should release its connection to the messaging system resources.</span></span> <span data-ttu-id="1fbc3-185">この操作を行った後、 **PR_STATUS_CODE**プロパティの STATUS_OFFLINE ビットを設定し、S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-185">After doing this, it should set the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property and return S_OK.</span></span> 
    
<span data-ttu-id="1fbc3-186">PROCESS_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="1fbc3-186">PROCESS_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="1fbc3-187">リモートトランスポートプロバイダーは、リモートメッセージを処理し、延期されたメッセージをすべてアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-187">The remote transport provider should process remote messages and upload any messages that have been deferred.</span></span> <span data-ttu-id="1fbc3-188">これを行うには、トランスポートプロバイダーは、ログオンオブジェクトの状態の行に次のプロパティ値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-188">To do this, the transport provider must set the following property values in the logon object's status row:</span></span>
    
   - <span data-ttu-id="1fbc3-189">**PR_STATUS_STRING**プロパティを、トランスポートプロバイダーのユーザーに対する状態を示す文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-189">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="1fbc3-190">**PR_STATUS_CODE**プロパティに STATUS_OUTBOUND_ENABLED および STATUS_OUTBOUND_ACTIVE ビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-190">Set the STATUS_OUTBOUND_ENABLED and STATUS_OUTBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="1fbc3-191">トランスポートプロバイダーの状態行の**PR_REMOTE_VALIDATE_OK**プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-191">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
   - <span data-ttu-id="1fbc3-192">**validatestate**が呼び出されたときに別の操作 (ヘッダーのダウンロードなど) が進行中の場合、 **validatestate**は MAPI_E_BUSY を返します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-192">If another operation is in progress (such as downloading headers) when **ValidateState** is called, **ValidateState** should return MAPI_E_BUSY.</span></span> 
    
   - <span data-ttu-id="1fbc3-193">REFRESH_XP_HEADER_CACHE フラグを処理するコードを実行して、Microsoft Exchange クライアントの要件を満たすようにします。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-193">Execute the code for processing the REFRESH_XP_HEADER_CACHE flag, as well, to satisfy requirements of the Microsoft Exchange client.</span></span>
    
<span data-ttu-id="1fbc3-194">REFRESH_XP_HEADER_CACHE</span><span class="sxs-lookup"><span data-stu-id="1fbc3-194">REFRESH_XP_HEADER_CACHE</span></span> 
  
> <span data-ttu-id="1fbc3-195">リモートトランスポートプロバイダーは、メッセージングシステムからすべての新しいメッセージヘッダーを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-195">The remote transport provider should retrieve any new message headers from the messaging system.</span></span> <span data-ttu-id="1fbc3-196">これを行うには、トランスポートプロバイダーは次のことを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-196">To do this, the transport provider must do the following:</span></span>
    
   - <span data-ttu-id="1fbc3-197">**PR_STATUS_STRING**プロパティを、トランスポートプロバイダーのユーザーに対する状態を示す文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-197">Set the **PR_STATUS_STRING** property to a string that indicates the transport provider's status to the user.</span></span> 
    
   - <span data-ttu-id="1fbc3-198">**PR_STATUS_CODE**プロパティに STATUS_INBOUND_ENABLED および STATUS_INBOUND_ACTIVE ビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-198">Set the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="1fbc3-199">**PR_STATUS_CODE**プロパティの STATUS_OFFLINE ビットをオフにします。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-199">Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="1fbc3-200">**PR_STATUS_CODE**プロパティの STATUS_ONLINE ビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-200">Set the STATUS_ONLINE bit in the **PR_STATUS_CODE** property.</span></span> 
    
   - <span data-ttu-id="1fbc3-201">トランスポートプロバイダーの状態行の**PR_REMOTE_VALIDATE_OK**プロパティを FALSE に設定します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-201">Set the **PR_REMOTE_VALIDATE_OK** property in the transport provider's status row to FALSE.</span></span> 
    
<span data-ttu-id="1fbc3-202">SHOW_XP_SESSION_UI</span><span class="sxs-lookup"><span data-stu-id="1fbc3-202">SHOW_XP_SESSION_UI</span></span> 
  
> <span data-ttu-id="1fbc3-203">メッセージヘッダー (メッセージのダウンロードを確認するダイアログボックスなど) を処理するためのユーザーインターフェイスがトランスポートプロバイダーにある場合は、そのダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-203">If your transport provider has any pieces of user interface for processing the message headers (such as a dialog box that confirms the downloading of messages), that dialog box should be displayed.</span></span> <span data-ttu-id="1fbc3-204">それ以外の場合、 **validatestate**は MAPI_E_NO_SUPPORT を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-204">Otherwise, **ValidateState** can return MAPI_E_NO_SUPPORT.</span></span> 
    
<span data-ttu-id="1fbc3-205">これら以外のフラグが渡された場合、 **validatestate**は MAPI_E_UNKNOWN_FLAGS を返さなければなりません。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-205">If any flags other than these are passed in, **ValidateState** should return MAPI_E_UNKNOWN_FLAGS.</span></span> 
  
<span data-ttu-id="1fbc3-206">多くの場合、トランスポートプロバイダーに対するクライアントの呼び出しは、 **imapistatus:: validatestate**メソッドになります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-206">The client's call to the transport provider will often be to the **IMAPIStatus::ValidateState** method.</span></span> <span data-ttu-id="1fbc3-207">**validatestate**の処理中は、トランスポートプロバイダーは、モデムや COM ポートなどの不足しているシステムリソースを割り当てるアクションを実行してはなりません。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-207">During the processing of **ValidateState**, the transport provider should not perform any actions that allocate scarce system resources, such as a modem or COM port.</span></span> <span data-ttu-id="1fbc3-208">これは、MAPI スプーラーが複数のトランスポートプロバイダーのキューをフラッシュする必要がある場合があるためです。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-208">This is because the MAPI spooler will sometimes need to flush queues on more than one transport provider.</span></span> <span data-ttu-id="1fbc3-209">ただし、クライアントは任意のトランスポートプロバイダーの**validatestate**メソッドをいつでも呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-209">However, the client can call any transport provider's **ValidateState** method at any time.</span></span> <span data-ttu-id="1fbc3-210">トランスポートプロバイダーが、 **validatestate**の処理中に希少でないリソースを割り当てようとした場合、MAPI スプーラーがキューをフラッシュするように指示した別のトランスポートプロバイダーとの競合が原因で、エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-210">If your transport provider attempts to allocate a scarce resource during the processing of **ValidateState**, an error can result due to conflict with another transport provider that the MAPI spooler has instructed to flush its queues.</span></span> <span data-ttu-id="1fbc3-211">すべての希少なリソース割り当てを MAPI スプーラーの方向で実行できるようにする場合は、このような競合を避けることができます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-211">If you allow all scarce resource allocations to occur under the direction of the MAPI spooler, you can avoid such conflicts.</span></span> <span data-ttu-id="1fbc3-212">トランスポートプロバイダーは**PR_REMOTE_VALIDATE_OK**プロパティをサポートしている必要があります。これにより、クライアントアプリケーションは、トランスポートプロバイダーがビジー状態になったとき、または MAPI スプーラーがアクションを開始するのを待っていることを検出できます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-212">Your transport provider should support the **PR_REMOTE_VALIDATE_OK** property so client applications can detect when your transport provider is busy or waiting for the MAPI spooler to initiate an action.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1fbc3-213">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="1fbc3-213">Notes to callers</span></span>

<span data-ttu-id="1fbc3-214">このメソッドを使用すると、その他の長い呼び出しが発生する可能性があるため、 **validatestate**は MAPI_E_BUSY を返して、このメソッドが別の操作の完了を待機していることを通知します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-214">Because this method can cause other potentially lengthy calls to be made, **ValidateState** can return MAPI_E_BUSY to inform you that this method is waiting for the completion of another operation.</span></span> <span data-ttu-id="1fbc3-215">別のタスクを試行する前に、保留中の操作が完了するまで待機する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-215">You should wait until the pending operation is complete before attempting another task.</span></span> 
  
<span data-ttu-id="1fbc3-216">トランスポートプロバイダーの状態オブジェクトに対する呼び出しを最も細かく制御できます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-216">You have the most control over your calls to transport provider status objects.</span></span> <span data-ttu-id="1fbc3-217">1つ以上のフラグを**validatestate**に渡して、トランスポートプロバイダーの操作に影響を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-217">You can pass one or more flags to **ValidateState** that affect the transport provider's operations.</span></span> <span data-ttu-id="1fbc3-218">たとえば、ABORT_XP_HEADER_OPERATION フラグは、ユーザーが入力規則を取り消したことを示します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-218">For example, the ABORT_XP_HEADER_OPERATION flag indicates that the user canceled the validation.</span></span> <span data-ttu-id="1fbc3-219">トランスポートプロバイダーは、中止、MAPI_E_USER_CANCELED を返す、または続行することを決定できます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-219">Transport providers can decide to abort, returning MAPI_E_USER_CANCELED, or can continue.</span></span> 
  
<span data-ttu-id="1fbc3-220">CONFIG_CHANGED フラグは、サービスプロバイダーまたは MAPI スプーラーの状態オブジェクトへの呼び出しに設定して、構成オプションが変更されたことを示すことができます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-220">You can set the CONFIG_CHANGED flag on a call to either the status object of a service provider or the MAPI spooler to indicate that a configuration option has been changed.</span></span> <span data-ttu-id="1fbc3-221">CONFIG_CHANGED を使用して、トランスポートプロバイダーを動的に再構成することができます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-221">You can use CONFIG_CHANGED to dynamically reconfigure a transport provider.</span></span> <span data-ttu-id="1fbc3-222">サービスプロバイダーの status オブジェクトへの呼び出しで CONFIG_CHANGED を設定すると、プロバイダーは[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)を呼び出して応答し、変更の MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-222">When you set CONFIG_CHANGED on a call to a service provider's status object, the provider responds with a call to [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) to alert the MAPI spooler of the change.</span></span> <span data-ttu-id="1fbc3-223">MAPI スプーラーの状態オブジェクトへの呼び出しで CONFIG_CHANGED を設定すると、スプーラーは各アクティブトランスポートプロバイダーに対して[IXPLogon:: AddressTypes](ixplogon-addresstypes.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-223">When you set CONFIG_CHANGED on a call to the MAPI spooler's status object, the spooler calls [IXPLogon::AddressTypes](ixplogon-addresstypes.md) for each active transport provider.</span></span> <span data-ttu-id="1fbc3-224">**AddressTypes**は、トランスポートのサポートされているアドレスの種類の MAPI スプーラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-224">**AddressTypes** informs the MAPI spooler of a transport's supported address types.</span></span> <span data-ttu-id="1fbc3-225">一部のサービスプロバイダーでは、検証に長い時間がかかることが予想される場合にも、進行状況のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-225">Some service providers also display a progress indicator if the validation is expected to take a long time.</span></span> <span data-ttu-id="1fbc3-226">進行状況インジケーターを表示することは便利ですが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-226">Displaying a progress indicator is helpful, but not required.</span></span> 
  
<span data-ttu-id="1fbc3-227">SUPPRESS_UI フラグが設定されている場合は、構成プロパティのシートまたは進行状況のダイアログボックスを表示できません。</span><span class="sxs-lookup"><span data-stu-id="1fbc3-227">When the SUPPRESS_UI flag is set, none of the configuration property sheets or progress dialog boxes can be displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1fbc3-228">関連項目</span><span class="sxs-lookup"><span data-stu-id="1fbc3-228">See also</span></span>

- [<span data-ttu-id="1fbc3-229">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="1fbc3-229">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
- [<span data-ttu-id="1fbc3-230">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="1fbc3-230">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
- [<span data-ttu-id="1fbc3-231">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1fbc3-231">IXPLogon::FlushQueues</span></span>](ixplogon-flushqueues.md)
- [<span data-ttu-id="1fbc3-232">PidTagRemoteValidateOk 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fbc3-232">PidTagRemoteValidateOk Canonical Property</span></span>](pidtagremotevalidateok-canonical-property.md)
- [<span data-ttu-id="1fbc3-233">PidTagResourceMethods 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fbc3-233">PidTagResourceMethods Canonical Property</span></span>](pidtagresourcemethods-canonical-property.md)
- [<span data-ttu-id="1fbc3-234">PidTagStatusCode 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fbc3-234">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)
- [<span data-ttu-id="1fbc3-235">PidTagStatusString 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1fbc3-235">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)
- [<span data-ttu-id="1fbc3-236">IMAPIStatus : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="1fbc3-236">IMAPIStatus : IMAPIProp</span></span>](imapistatusimapiprop.md)

