---
title: IMAPIFolderCopyMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: 4c7d2110-3fcb-4b9f-bf20-1dc1a611161d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424456"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="0a9f0-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="0a9f0-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="0a9f0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a9f0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a9f0-105">1 つ以上のメッセージをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-105">Copies or moves one or more messages.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPENTRYLIST lpMsgList,
  LPCIID lpInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0a9f0-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0a9f0-106">Parameters</span></span>

 <span data-ttu-id="0a9f0-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="0a9f0-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="0a9f0-108">[in]コピーまたは移動するメッセージを識別する [ENTRYLIST](entrylist.md) 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="0a9f0-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="0a9f0-109">_lpInterface_</span></span>
  
> <span data-ttu-id="0a9f0-110">[in]  _lpDestFolder_ パラメーターが指す移動先フォルダーにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="0a9f0-111">NULL を渡した場合、サービス プロバイダーは標準のフォルダー インターフェイス [IMAPIFolder : IMAPIContainer を返します](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="0a9f0-112">クライアントは NULL を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-112">Clients must pass NULL.</span></span> <span data-ttu-id="0a9f0-113">他の呼び出し元は  _、lpInterface_ パラメーターを、IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、またはIID_IMAPIFolder。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="0a9f0-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="0a9f0-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="0a9f0-115">[in]コピーまたは移動されたメッセージを受信する開いているフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="0a9f0-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0a9f0-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="0a9f0-117">[in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="0a9f0-118">_ulUIParam_ パラメーターは、クライアントが _ulFlags_ パラメーターに MESSAGE_DIALOG フラグを設定し _、lpProgress_ パラメーターに NULL を渡す場合を無視します。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="0a9f0-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="0a9f0-119">_lpProgress_</span></span>
  
> <span data-ttu-id="0a9f0-120">[in]進行状況インジケーターを表示する進行状況オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="0a9f0-121">_lpProgress_ で NULL が渡された場合、メッセージ ストア プロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="0a9f0-122">_lpProgress パラメーター_ は _、ulFlags_ で MESSAGE_DIALOGフラグが設定されていない限り無視されます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="0a9f0-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0a9f0-123">_ulFlags_</span></span>
  
> <span data-ttu-id="0a9f0-124">[in]コピーまたは移動操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="0a9f0-125">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-125">The following flags can be set:</span></span>
    
<span data-ttu-id="0a9f0-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="0a9f0-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="0a9f0-127">サポート オブジェクトの [IMAPISupport::D oCopyTo](imapisupport-docopyto.md)または [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md)メソッドを呼び出して **、IMAPIFolder::CopyMessages** を実装している場合は、メッセージ ストア プロバイダーに直ちに MAPI_E_DECLINE_COPY を返す通知を行います。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="0a9f0-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0a9f0-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="0a9f0-129">操作が進むにつれて進行状況インジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="0a9f0-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="0a9f0-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="0a9f0-131">メッセージまたはメッセージは、コピーの代わりに移動されます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="0a9f0-132">このMESSAGE_MOVE設定されていない場合は、メッセージがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0a9f0-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="0a9f0-133">Return value</span></span>

<span data-ttu-id="0a9f0-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a9f0-134">S_OK</span></span> 
  
> <span data-ttu-id="0a9f0-135">メッセージまたはメッセージが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="0a9f0-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="0a9f0-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="0a9f0-137">プロバイダーは、サポート オブジェクト メソッドを呼び出してこのメソッドを実装し、呼び出し元が MAPI_DECLINE_OK渡しました。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="0a9f0-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="0a9f0-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="0a9f0-139">呼び出しは成功しましたが、すべてのエントリが正常にコピーまたは移動されたという訳ではありません。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="0a9f0-140">この警告が返されると、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="0a9f0-141">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="0a9f0-142">詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a9f0-143">注釈</span><span class="sxs-lookup"><span data-stu-id="0a9f0-143">Remarks</span></span>

<span data-ttu-id="0a9f0-144">**IMAPIFolder::CopyMessages メソッドは**、メッセージを別のフォルダーにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="0a9f0-145">読み取り/書き込み権限で開いたメッセージは、移動またはコピーできます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="0a9f0-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="0a9f0-146">Notes to implementers</span></span>

<span data-ttu-id="0a9f0-147">[IMAPISupport::CopyMessages](imapisupport-copymessages.md)メソッドを使用せずに別のメッセージ ストアにメッセージをコピーする場合は、最初に[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)を GENERATE_RECEIPT_ONLY フラグ セットで呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="0a9f0-148">受信メッセージ ストアは、コピーまたは移動されたメッセージの読み取りレポートを生成する責任を負いません。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="0a9f0-149">**IMAPISupport::CopyMessages** を呼び出して **IMAPIFolder::CopyMessages** を実装する場合は **、SetReadFlags を呼び出さない**。MAPI が呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="0a9f0-150">実装では、メッセージを任意の順序で移動またはコピーし、任意の順序で読み取り状態レポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="0a9f0-151">つまり、メッセージのコピーを完了してから、読み取り状態レポートを生成するか、または実装がコピー操作を開始する前にレポートを送信できます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="0a9f0-152">ただし、コピーが成功したかどうかに関係なく、すべてのメッセージをコピーするために読み取りレポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="0a9f0-153">コピー操作または移動操作に複数のメッセージが含まれる場合は、可能な限り完全に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="0a9f0-154">メモリの使い切れ、ディスク領域の使い切れ、メッセージ ストアの破損など、制御できないエラーが発生しない限り、操作を途中で停止しません。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="0a9f0-155">移動操作またはコピー操作全体でエントリ識別子を維持してみてください。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="0a9f0-156">必須ではないが、エントリ識別子も保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="0a9f0-157">メッセージを移動またはコピーするときに通知を送信し、クライアントがメッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドへの呼び出しが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="0a9f0-158">コピーまたは移動操作にメッセージの状態を含めない。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="0a9f0-159">メッセージの状態を移動またはコピーすると、パフォーマンスに大きな影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0a9f0-160">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0a9f0-160">Notes to callers</span></span>

<span data-ttu-id="0a9f0-161">**IMAPIFolder::CopyMessages** を使用して検索結果フォルダーを作成します。メッセージは多くの場合、親フォルダーでグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="0a9f0-162">これらの戻り値は、次の条件下で期待してください。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="0a9f0-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="0a9f0-163">**Condition**</span></span>|<span data-ttu-id="0a9f0-164">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="0a9f0-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a9f0-165">**IMAPIFolder::CopyMessages は** 、すべてのメッセージを正常にコピーまたは移動しました。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="0a9f0-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a9f0-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="0a9f0-167">**IMAPIFolder::CopyMessages** は、すべてのメッセージを正常にコピーまたは移動できなかった。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="0a9f0-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="0a9f0-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="0a9f0-169">**IMAPIFolder::CopyMessages** を完了できません。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="0a9f0-170">エラー値</span><span class="sxs-lookup"><span data-stu-id="0a9f0-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="0a9f0-171">**IMAPIFolder::CopyMessages** を完了できない場合は、作業が完了していないと想定しません。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="0a9f0-172">**IMAPIFolder::CopyMessages は** 、エラーが発生する前に 1 つ以上のメッセージをコピーまたは移動できた可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0a9f0-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a9f0-173">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a9f0-173">See also</span></span>



[<span data-ttu-id="0a9f0-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="0a9f0-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

