---
title: imapifoldercopymessages
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
ms.openlocfilehash: 21aa28e1a2c11ee7361fb4921f8d527b3e3ceb44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280128"
---
# <a name="imapifoldercopymessages"></a><span data-ttu-id="363a6-103">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="363a6-103">IMAPIFolder::CopyMessages</span></span>

  
  
<span data-ttu-id="363a6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="363a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="363a6-105">1つまたは複数のメッセージをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="363a6-105">Copies or moves one or more messages.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="363a6-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="363a6-106">Parameters</span></span>

 <span data-ttu-id="363a6-107">_lpmsglist_</span><span class="sxs-lookup"><span data-stu-id="363a6-107">_lpMsgList_</span></span>
  
> <span data-ttu-id="363a6-108">順番コピーまたは移動するメッセージを識別する[entrylist](entrylist.md)構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="363a6-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that identify the message or messages to copy or move.</span></span> 
    
 <span data-ttu-id="363a6-109">_lpinterface_</span><span class="sxs-lookup"><span data-stu-id="363a6-109">_lpInterface_</span></span>
  
> <span data-ttu-id="363a6-110">順番_lpdestfolder_パラメーターによって指定された宛先フォルダーへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。</span><span class="sxs-lookup"><span data-stu-id="363a6-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder pointed to by the  _lpDestFolder_ parameter.</span></span> <span data-ttu-id="363a6-111">サービスプロバイダーに NULL 結果が渡され、標準のフォルダーインターフェイス、 [imapifolder: IMAPIContainer](imapifolderimapicontainer.md)が返されます。</span><span class="sxs-lookup"><span data-stu-id="363a6-111">Passing NULL results in the service provider returning the standard folder interface, [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md).</span></span> <span data-ttu-id="363a6-112">クライアントは、NULL を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="363a6-112">Clients must pass NULL.</span></span> <span data-ttu-id="363a6-113">他の呼び出し元が_lpinterface_パラメーターを IID_IUnknown、IID_IMAPIProp、IID_IMAPIContainer、または IID_IMAPIFolder に設定できます。</span><span class="sxs-lookup"><span data-stu-id="363a6-113">Other callers can set the  _lpInterface_ parameter to IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, or IID_IMAPIFolder.</span></span> 
    
 <span data-ttu-id="363a6-114">_lpdestfolder_</span><span class="sxs-lookup"><span data-stu-id="363a6-114">_lpDestFolder_</span></span>
  
> <span data-ttu-id="363a6-115">順番コピーまたは移動されたメッセージを受信する、開いているフォルダーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="363a6-115">[in] A pointer to the open folder to receive the copied or moved messages.</span></span>
    
 <span data-ttu-id="363a6-116">_uluiparam_</span><span class="sxs-lookup"><span data-stu-id="363a6-116">_ulUIParam_</span></span>
  
> <span data-ttu-id="363a6-117">順番このメソッドが表示する任意のダイアログボックスまたはウィンドウの親ウィンドウへのハンドル。</span><span class="sxs-lookup"><span data-stu-id="363a6-117">[in] A handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="363a6-118">_uluiparam_パラメーターは、クライアントが_ulflags_パラメーターに MESSAGE_DIALOG フラグを設定し、 _lpprogress_パラメーターに NULL を渡す場合を除き、無視されます。</span><span class="sxs-lookup"><span data-stu-id="363a6-118">The  _ulUIParam_ parameter is ignored unless the client sets the MESSAGE_DIALOG flag in the  _ulFlags_ parameter and passes NULL in the  _lpProgress_ parameter.</span></span> 
    
 <span data-ttu-id="363a6-119">_lpprogress_</span><span class="sxs-lookup"><span data-stu-id="363a6-119">_lpProgress_</span></span>
  
> <span data-ttu-id="363a6-120">順番進行状況インジケーターを表示する progress オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="363a6-120">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="363a6-121">_lpprogress_で NULL が渡された場合、メッセージストアプロバイダーは MAPI 進行状況オブジェクトの実装を使用して進行状況インジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="363a6-121">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="363a6-122">MESSAGE_DIALOG フラグが_ulflags_で設定されていない場合、 _lpprogress_パラメーターは無視されます。</span><span class="sxs-lookup"><span data-stu-id="363a6-122">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="363a6-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="363a6-123">_ulFlags_</span></span>
  
> <span data-ttu-id="363a6-124">順番コピー操作または移動操作の実行方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="363a6-124">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="363a6-125">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="363a6-125">The following flags can be set:</span></span>
    
<span data-ttu-id="363a6-126">MAPI_DECLINE_OK</span><span class="sxs-lookup"><span data-stu-id="363a6-126">MAPI_DECLINE_OK</span></span> 
  
> <span data-ttu-id="363a6-127">サポートオブジェクトの[imapifolder::D ocopyto](imapisupport-docopyto.md)または[imapifolder::D ocopyprops](imapisupport-docopyprops.md)メソッドを呼び出して、 **imapifolder:: copymessages**を実装することによって、メッセージストアプロバイダーに直ちに MAPI_E_DECLINE_COPY を返すように通知します。</span><span class="sxs-lookup"><span data-stu-id="363a6-127">Informs the message store provider to immediately return MAPI_E_DECLINE_COPY if it implements **IMAPIFolder::CopyMessages** by calling the support object's [IMAPISupport::DoCopyTo](imapisupport-docopyto.md) or [IMAPISupport::DoCopyProps](imapisupport-docopyprops.md) method.</span></span> 
    
<span data-ttu-id="363a6-128">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="363a6-128">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="363a6-129">操作の進行状況を示すインジケーターを表示します。</span><span class="sxs-lookup"><span data-stu-id="363a6-129">Displays a progress indicator as the operation proceeds.</span></span>
    
<span data-ttu-id="363a6-130">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="363a6-130">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="363a6-131">メッセージをコピーではなく移動します。</span><span class="sxs-lookup"><span data-stu-id="363a6-131">The message or messages are to be moved instead of copied.</span></span> <span data-ttu-id="363a6-132">MESSAGE_MOVE が設定されていない場合は、メッセージがコピーされます。</span><span class="sxs-lookup"><span data-stu-id="363a6-132">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="363a6-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="363a6-133">Return value</span></span>

<span data-ttu-id="363a6-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="363a6-134">S_OK</span></span> 
  
> <span data-ttu-id="363a6-135">メッセージまたはメッセージが正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="363a6-135">The message or messages have been successfully copied or moved.</span></span>
    
<span data-ttu-id="363a6-136">MAPI_E_DECLINE_COPY</span><span class="sxs-lookup"><span data-stu-id="363a6-136">MAPI_E_DECLINE_COPY</span></span> 
  
> <span data-ttu-id="363a6-137">プロバイダーは、サポートオブジェクトのメソッドを呼び出すことによってこのメソッドを実装し、発信者が MAPI_DECLINE_OK フラグを渡しています。</span><span class="sxs-lookup"><span data-stu-id="363a6-137">The provider implements this method by calling a support object method, and the caller has passed the MAPI_DECLINE_OK flag.</span></span>
    
<span data-ttu-id="363a6-138">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="363a6-138">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="363a6-139">呼び出しは成功しましたが、すべてのエントリが正常にコピーまたは移動されませんでした。</span><span class="sxs-lookup"><span data-stu-id="363a6-139">The call succeeded, but not all entries were successfully copied or moved.</span></span> <span data-ttu-id="363a6-140">この警告が返された場合、呼び出しは正常に処理されます。</span><span class="sxs-lookup"><span data-stu-id="363a6-140">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="363a6-141">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="363a6-141">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="363a6-142">詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="363a6-142">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="363a6-143">解説</span><span class="sxs-lookup"><span data-stu-id="363a6-143">Remarks</span></span>

<span data-ttu-id="363a6-144">**imapifolder:: copymessages**メソッドは、メッセージを別のフォルダーにコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="363a6-144">The **IMAPIFolder::CopyMessages** method copies or moves messages to another folder.</span></span> 
  
<span data-ttu-id="363a6-145">読み取り/書き込みアクセス許可を使用して開かれたメッセージは、移動またはコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="363a6-145">Messages that are opened with read/write permission can be moved or copied.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="363a6-146">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="363a6-146">Notes to implementers</span></span>

<span data-ttu-id="363a6-147">[imapisupport:: copymessages](imapisupport-copymessages.md)メソッドを使用せずにメッセージを別のメッセージストアにコピーする場合は、GENERATE_RECEIPT_ONLY フラグが設定された[imapisupport:: setreadflags](imapifolder-setreadflags.md)を最初に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="363a6-147">If you are copying messages to another message store without using the [IMAPISupport::CopyMessages](imapisupport-copymessages.md) method, you must first call [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) with the GENERATE_RECEIPT_ONLY flag set.</span></span> <span data-ttu-id="363a6-148">受信側のメッセージストアは、コピーまたは移動されたメッセージの読み取りレポートを生成する責任がありません。</span><span class="sxs-lookup"><span data-stu-id="363a6-148">The receiving message store is not responsible for generating read reports for the copied or moved messages.</span></span> <span data-ttu-id="363a6-149">**imapisupport:** : copymessages を呼び出して**imapisupport:: copymessages**を実装する場合は、 **setreadflags**を呼び出さないでください。MAPI がこれを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="363a6-149">If you are calling **IMAPISupport::CopyMessages** to implement **IMAPIFolder::CopyMessages**, do not call **SetReadFlags**; MAPI will call it.</span></span> 
  
<span data-ttu-id="363a6-150">実装では、任意の順序でメッセージを移動またはコピーしたり、読み取り状態レポートを生成したりできます。</span><span class="sxs-lookup"><span data-stu-id="363a6-150">Your implementation can move or copy the messages in any order and generate read status reports in any order.</span></span> <span data-ttu-id="363a6-151">つまり、読み取り状態レポートを生成する前にメッセージのコピーを終了するか、または実装でコピー操作を開始する前にレポートを送信することができます。</span><span class="sxs-lookup"><span data-stu-id="363a6-151">That is, you can finish copying messages before generating any of the read status reports or send the reports before your implementation starts the copy operation.</span></span> <span data-ttu-id="363a6-152">ただし、コピーが成功したかどうかにかかわらず、すべてのメッセージをコピーするには、読み取りレポートを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="363a6-152">However, read reports should be sent for all messages to be copied, regardless of whether the copy is successful.</span></span>
  
<span data-ttu-id="363a6-153">コピー操作または移動操作に複数のメッセージが含まれている場合は、操作をできるだけ完全に実行します。</span><span class="sxs-lookup"><span data-stu-id="363a6-153">When the copy or move operation involves more than one message, perform the operation as completely as possible.</span></span> <span data-ttu-id="363a6-154">メモリが不足している、ディスクの空き領域が不足している、メッセージストアが破損しているなど、操作を途中で停止しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="363a6-154">Do not stop the operation prematurely unless a failure occurs that is beyond your control, such as running out of memory, running out of disk space, or corruption in the message store.</span></span>
  
<span data-ttu-id="363a6-155">移動操作またはコピー操作の間にエントリ識別子を保持するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="363a6-155">Try to maintain entry identifiers across move or copy operations.</span></span> <span data-ttu-id="363a6-156">エントリ識別子も保持する必要がありますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="363a6-156">You should also preserve entry identifiers, although it is not required.</span></span>
  
<span data-ttu-id="363a6-157">メッセージを移動またはコピーするときに通知を送信します。そのため、クライアントは、メッセージ ' [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドへの呼び出しが失敗する可能性があることを forewarned します。</span><span class="sxs-lookup"><span data-stu-id="363a6-157">Send notifications when you move or copy messages so that clients are forewarned that their calls to the messages' [IMAPIProp::SaveChanges](imapiprop-savechanges.md) methods may fail.</span></span> 
  
<span data-ttu-id="363a6-158">コピー操作または移動操作では、メッセージの状態は含まれません。</span><span class="sxs-lookup"><span data-stu-id="363a6-158">Do not include a message's status in the copy or move operation.</span></span> <span data-ttu-id="363a6-159">メッセージの状態を移動またはコピーすると、パフォーマンスに大きく影響します。</span><span class="sxs-lookup"><span data-stu-id="363a6-159">Moving or copying a message status greatly affects performance.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="363a6-160">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="363a6-160">Notes to callers</span></span>

<span data-ttu-id="363a6-161">**imapifolder:: copymessages**を使用して、メッセージが親フォルダーによってグループ化されることが多い検索結果フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="363a6-161">Use **IMAPIFolder::CopyMessages** to populate search-results folders, where messages are often grouped by parent folder.</span></span> 
  
<span data-ttu-id="363a6-162">これらの戻り値は、次の条件に当てはまることが予想されます。</span><span class="sxs-lookup"><span data-stu-id="363a6-162">Expect these return values under the following conditions.</span></span>
  
|<span data-ttu-id="363a6-163">**Condition**</span><span class="sxs-lookup"><span data-stu-id="363a6-163">**Condition**</span></span>|<span data-ttu-id="363a6-164">**戻り値**</span><span class="sxs-lookup"><span data-stu-id="363a6-164">**Return value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="363a6-165">**imapifolder:: copymessages**は、すべてのメッセージで正常にコピーまたは移動されました。</span><span class="sxs-lookup"><span data-stu-id="363a6-165">**IMAPIFolder::CopyMessages** has successfully copied or moved every message.</span></span>  <br/> |<span data-ttu-id="363a6-166">S_OK</span><span class="sxs-lookup"><span data-stu-id="363a6-166">S_OK</span></span>  <br/> |
|<span data-ttu-id="363a6-167">**imapifolder:: copymessages**は、すべてのメッセージを正常にコピーまたは移動できませんでした。</span><span class="sxs-lookup"><span data-stu-id="363a6-167">**IMAPIFolder::CopyMessages** was unable to successfully copy or move every message.</span></span>  <br/> |<span data-ttu-id="363a6-168">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="363a6-168">MAPI_W_PARTIAL_COMPLETION</span></span>  <br/> |
|<span data-ttu-id="363a6-169">**imapifolder:: copymessages**を完了できませんでした。</span><span class="sxs-lookup"><span data-stu-id="363a6-169">**IMAPIFolder::CopyMessages** was unable to complete.</span></span>  <br/> |<span data-ttu-id="363a6-170">任意のエラー値</span><span class="sxs-lookup"><span data-stu-id="363a6-170">Any error value</span></span>  <br/> |
   
<span data-ttu-id="363a6-171">**imapifolder:: copymessages**を完了できない場合は、作業が行われていないと仮定しません。</span><span class="sxs-lookup"><span data-stu-id="363a6-171">When **IMAPIFolder::CopyMessages** is unable to complete, do not assume that no work was done.</span></span> <span data-ttu-id="363a6-172">**imapifolder:: copymessages**は、エラーが発生する前に1つ以上のメッセージをコピーまたは移動できる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="363a6-172">**IMAPIFolder::CopyMessages** might have been able to copy or move one or more messages before encountering the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="363a6-173">関連項目</span><span class="sxs-lookup"><span data-stu-id="363a6-173">See also</span></span>



[<span data-ttu-id="363a6-174">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="363a6-174">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

