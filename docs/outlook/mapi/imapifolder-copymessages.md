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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e253aa6a701d565fbc61e8a0e0a6388f7199c000
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593264"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="7a94a-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="7a94a-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="7a94a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a94a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a94a-105">1 つまたは複数のメッセージを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="7a94a-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="7a94a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7a94a-106">Parameters</span></span>

 <span data-ttu-id="7a94a-107">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="7a94a-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="7a94a-108">[in]メッセージまたはメッセージのコピーまたは移動を識別する[ENTRYLIST](entrylist.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a94a-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="7a94a-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7a94a-109">_lpInterface_</span></span>
  
> <span data-ttu-id="7a94a-110">[in]_LpDestFolder_パラメーターで指定された移動先フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a94a-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="7a94a-111">フォルダーの標準的なインターフェイスを返すサービス プロバイダーの結果をパラメーターに NULL [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)。</span><span class="sxs-lookup"><span data-stu-id="7a94a-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="7a94a-112">クライアントでは、NULL を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a94a-112">Clients must pass NULL.</span></span> <span data-ttu-id="7a94a-113">他の呼び出し元に対する、IID_IMAPIProp、IID_IMAPIContainer、または IID_IMAPIFolder、 _lpInterface_パラメーターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="7a94a-114">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="7a94a-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="7a94a-115">[in]開いているフォルダーにコピーまたは移動されたメッセージを受信するへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a94a-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="7a94a-116">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="7a94a-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="7a94a-117">[in]ダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドルを表示します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="7a94a-118">_UlUIParam_パラメーターは、クライアントは、 _ulFlags_パラメーターに MESSAGE_DIALOG フラグを設定し、 _lpProgress_パラメーターに NULL を渡す場合を除き、無視されます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="7a94a-119">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="7a94a-119">_lpProgress_</span></span>
  
> <span data-ttu-id="7a94a-120">[in]進行状況インジケーターを表示する進行中のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a94a-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="7a94a-121">_LpProgress_に NULL を渡した場合、メッセージ ストア プロバイダーは、MAPI 処理中のオブジェクトの実装を使用して進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="7a94a-122">_UlFlags_に MESSAGE_DIALOG フラグが設定されていない限り、 _lpProgress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="7a94a-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a94a-123">_ulFlags_</span></span>
  
> <span data-ttu-id="7a94a-124">[in]コピーまたは移動操作を実現する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="7a94a-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="7a94a-125">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-125">The following flags can be set:</span></span>
    
<span data-ttu-id="7a94a-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="7a94a-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="7a94a-127">サポート オブジェクトの[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)または[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)メソッドを呼び出すことによって**IMAPIFolder::CopyMessages**を実装している場合に MAPI_E_DECLINE_COPY をすぐに返すメッセージ ストア プロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="7a94a-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="7a94a-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="7a94a-129">操作の進行中は、進行状況のインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="7a94a-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="7a94a-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="7a94a-131">代わりに移動するのには、メッセージまたはメッセージをコピーします。</span><span class="sxs-lookup"><span data-stu-id="7a94a-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="7a94a-132">MESSAGE_MOVE が設定されていない場合、メッセージがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a94a-133">�߂�l</span><span class="sxs-lookup"><span data-stu-id="7a94a-133">Return value</span></span>

<span data-ttu-id="7a94a-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a94a-134">S_OK</span></span> 
  
> <span data-ttu-id="7a94a-135">メッセージまたはメッセージがされて正常にコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="7a94a-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="7a94a-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="7a94a-137">プロバイダーのサポートのオブジェクトのメソッドを呼び出すことによってこのメソッドを実装して、呼び出し元に MAPI_DECLINE_OK フラグが渡されます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="7a94a-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7a94a-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="7a94a-139">呼び出しが成功したが、すべてのエントリが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="7a94a-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="7a94a-140">この警告が返されると、呼び出しを成功として処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a94a-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="7a94a-141">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="7a94a-142">詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a94a-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a94a-143">注釈</span><span class="sxs-lookup"><span data-stu-id="7a94a-143">Remarks</span></span>

<span data-ttu-id="7a94a-144">**IMAPIFolder::CopyMessages**メソッドは、コピーまたは別のフォルダーにメッセージを移動します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="7a94a-145">開かれているメッセージ読み取り/書き込みアクセス許可を移動またはコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a94a-146">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="7a94a-146">Notes to implementers</span></span>

<span data-ttu-id="7a94a-147">[IMAPISupport::CopyMessages](imapisupport-copymessages.md)メソッドを使用せず、別のメッセージ ストアにメッセージをコピーする場合は、GENERATE_RECEIPT_ONLY フラグを設定して[IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)を最初に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a94a-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="7a94a-148">受信側メッセージ ・ ストアは、コピーまたは移動されたメッセージの読み取りのレポートを生成するための責任ではありません。</span><span class="sxs-lookup"><span data-stu-id="7a94a-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="7a94a-149">場合は**IMAPIFolder::CopyMessages**を実装するために**IMAPISupport::CopyMessages**を呼び出す場合、呼び出さないように**SetReadFlags**。MAPI を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="7a94a-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="7a94a-150">実装は、移動または任意の順序でメッセージをコピーし、任意の順序で読み取りステータス レポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="7a94a-151">読み取りステータス レポートを生成する前にメッセージのコピーを完了したり、実装は、コピー操作を開始する前にレポートを送信できます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="7a94a-152">ただし、コピーが成功するかどうかに関係なく、コピーするすべてのメッセージを送信するレポートを読みます。</span><span class="sxs-lookup"><span data-stu-id="7a94a-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="7a94a-153">コピーまたは移動操作には、複数のメッセージが含まれている場合は、できるだけ完全に操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="7a94a-154">メモリが不足している、ディスク領域、またはメッセージ ・ ストア内の破損が不足しているなど、ユーザーが制御できない障害が発生した場合を除きは、処理の途中で操作を停止しません。</span><span class="sxs-lookup"><span data-stu-id="7a94a-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="7a94a-155">移動またはコピー操作の間でのエントリの識別子を維持しようとしてください。</span><span class="sxs-lookup"><span data-stu-id="7a94a-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="7a94a-156">必須ではありませんが、エントリの識別子を維持することもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a94a-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="7a94a-157">移動またはクライアントがメッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出しは失敗する可能性があることあらかじめご了承するようにメッセージをコピーするときに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="7a94a-158">メッセージの状態は、コピー、移動の操作をしたりしないでください。</span><span class="sxs-lookup"><span data-stu-id="7a94a-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="7a94a-159">移動またはメッセージの状態のコピーを大幅にパフォーマンスに影響します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7a94a-160">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7a94a-160">Notes to callers</span></span>

<span data-ttu-id="7a94a-161">**IMAPIFolder::CopyMessages**を使用して、検索結果のフォルダー、メッセージ多くの場合、親フォルダー グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="7a94a-162">次の条件下で、これらの戻り値を期待してください。</span><span class="sxs-lookup"><span data-stu-id="7a94a-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="7a94a-163">**条件**</span><span class="sxs-lookup"><span data-stu-id="7a94a-163">**Condition**</span></span>|<span data-ttu-id="7a94a-164">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="7a94a-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7a94a-165">**IMAPIFolder::CopyMessages**が正常にコピーまたは、すべてのメッセージを移動します。</span><span class="sxs-lookup"><span data-stu-id="7a94a-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="7a94a-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a94a-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="7a94a-167">**IMAPIFolder::CopyMessages**は、正常にコピーまたはすべてのメッセージを移動できませんでした。</span><span class="sxs-lookup"><span data-stu-id="7a94a-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="7a94a-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="7a94a-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="7a94a-169">**IMAPIFolder::CopyMessages**は完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="7a94a-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="7a94a-170">エラー値</span><span class="sxs-lookup"><span data-stu-id="7a94a-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="7a94a-171">**IMAPIFolder::CopyMessages**が完了することではない場合と仮定しないでその作業は実行されませんでした。</span><span class="sxs-lookup"><span data-stu-id="7a94a-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="7a94a-172">**IMAPIFolder::CopyMessages**は、コピーまたはエラーが発生する前に 1 つまたは複数のメッセージを移動することがされている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7a94a-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a94a-173">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a94a-173">See also</span></span>



[<span data-ttu-id="7a94a-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="7a94a-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

