---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418639"
---
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="25222-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="25222-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="25222-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25222-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25222-105">特定のフォルダー内のメッセージに関連付けられている状態を取得します (たとえば、そのメッセージが削除のマークが付けられているかどうかなど)。</span><span class="sxs-lookup"><span data-stu-id="25222-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="25222-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="25222-106">Parameters</span></span>

 <span data-ttu-id="25222-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="25222-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="25222-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="25222-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="25222-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="25222-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="25222-110">[in]状態が取得されたメッセージのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="25222-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="25222-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="25222-111">_ulFlags_</span></span>
  
> <span data-ttu-id="25222-112">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="25222-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="25222-113">_lpulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="25222-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="25222-114">[out]メッセージの状態を示すフラグのビットマスクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="25222-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="25222-115">ビット 0 ~ 15 は予約済みで、ゼロである必要があります。ビット 16 ~ 31 は、実装固有の使用に使用できます。</span><span class="sxs-lookup"><span data-stu-id="25222-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="25222-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="25222-116">The following flags can be set:</span></span>
    
<span data-ttu-id="25222-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="25222-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="25222-118">メッセージが削除のマークが付いている。</span><span class="sxs-lookup"><span data-stu-id="25222-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="25222-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="25222-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="25222-120">メッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="25222-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="25222-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="25222-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="25222-122">メッセージが強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="25222-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="25222-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="25222-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="25222-124">メッセージは、ローカル クライアントにダウンロードせずにリモート メッセージ ストアで削除のマークが付けされています。</span><span class="sxs-lookup"><span data-stu-id="25222-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="25222-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="25222-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="25222-126">メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロードするマークが付けされています。</span><span class="sxs-lookup"><span data-stu-id="25222-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="25222-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="25222-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="25222-128">メッセージは、クライアント定義の目的でタグ付けされています。</span><span class="sxs-lookup"><span data-stu-id="25222-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="25222-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="25222-129">Return value</span></span>

<span data-ttu-id="25222-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="25222-130">S_OK</span></span> 
  
> <span data-ttu-id="25222-131">メッセージの状態が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="25222-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="25222-132">注釈</span><span class="sxs-lookup"><span data-stu-id="25222-132">Remarks</span></span>

<span data-ttu-id="25222-133">**IMAPIFolder::GetMessageStatus** メソッドは、メッセージの状態を返します。</span><span class="sxs-lookup"><span data-stu-id="25222-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="25222-134">メッセージの状態は、メッセージのプロパティ ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md) **)** PR_MSG_STATUSに格納されます。</span><span class="sxs-lookup"><span data-stu-id="25222-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="25222-135">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="25222-135">Notes to implementers</span></span>

<span data-ttu-id="25222-136">メッセージの状態ビットの設定方法、クリア方法、および使用方法は、実装によって完全に異なりますが、ビット 0 ~ 15 は予約済みで、ゼロである必要があります。</span><span class="sxs-lookup"><span data-stu-id="25222-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="25222-137">IPM サブツリーにメッセージを格納する場合、MAPI は IPM クライアントで使用するためにビット 16 ~ 31 を予約します。</span><span class="sxs-lookup"><span data-stu-id="25222-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="25222-138">他のサブツリーにメッセージを格納する場合は、ビット 16 ~ 31 を独自の目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="25222-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="25222-139">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="25222-139">MFCMAPI reference</span></span>

<span data-ttu-id="25222-140">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25222-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="25222-141">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="25222-141">**File**</span></span>|<span data-ttu-id="25222-142">**関数**</span><span class="sxs-lookup"><span data-stu-id="25222-142">**Function**</span></span>|<span data-ttu-id="25222-143">**コメント**</span><span class="sxs-lookup"><span data-stu-id="25222-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="25222-144">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="25222-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="25222-145">CMyMAPIFormViewer::GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="25222-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="25222-146">MFCMAPI は **IMAPIFolder::GetMessageStatus** メソッドを使用して、表示する次のメッセージの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="25222-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="25222-147">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="25222-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="25222-148">OpenMessageNonModal と OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="25222-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="25222-149">MFCMAPI は **IMAPIFolder::GetMessageStatus** メソッドを使用して、表示するメッセージの状態を取得してフォーム ビューアーに渡します。これは CMyMAPIFormViewer または [IMAPISession::ShowForm](imapisession-showform.md)です。</span><span class="sxs-lookup"><span data-stu-id="25222-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25222-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="25222-150">See also</span></span>



[<span data-ttu-id="25222-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="25222-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="25222-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="25222-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="25222-153">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="25222-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="25222-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="25222-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="25222-155">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="25222-155">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

