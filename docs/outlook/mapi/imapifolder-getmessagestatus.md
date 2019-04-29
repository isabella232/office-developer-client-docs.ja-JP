---
title: imapifoldergetmessagestatus
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
# <a name="imapifoldergetmessagestatus"></a><span data-ttu-id="c0009-103">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="c0009-103">IMAPIFolder::GetMessageStatus</span></span>

  
  
<span data-ttu-id="c0009-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0009-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0009-105">特定のフォルダー内のメッセージに関連付けられている状態を取得します (たとえば、そのメッセージに削除のマークが付いているかどうか)。</span><span class="sxs-lookup"><span data-stu-id="c0009-105">Obtains the status associated with a message in a particular folder (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a><span data-ttu-id="c0009-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c0009-106">Parameters</span></span>

 <span data-ttu-id="c0009-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="c0009-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="c0009-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="c0009-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="c0009-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="c0009-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="c0009-110">順番状態が取得されるメッセージのエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c0009-110">[in] A pointer to the entry identifier for the message whose status is obtained.</span></span>
    
 <span data-ttu-id="c0009-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c0009-111">_ulFlags_</span></span>
  
> <span data-ttu-id="c0009-112">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="c0009-112">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c0009-113">_lアウト messagestatus_</span><span class="sxs-lookup"><span data-stu-id="c0009-113">_lpulMessageStatus_</span></span>
  
> <span data-ttu-id="c0009-114">読み上げメッセージの状態を示すフラグのビットマスクへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="c0009-114">[out] A pointer to a pointer to a bitmask of flags that indicate the message's status.</span></span> <span data-ttu-id="c0009-115">ビット 0 ~ 15 は予約されており、0である必要があります。bits 16 ~ 31 は実装固有の用途に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c0009-115">Bits 0 through 15 are reserved and must be zero; bits 16 through 31 are available for implementation-specific use.</span></span> <span data-ttu-id="c0009-116">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="c0009-116">The following flags can be set:</span></span>
    
<span data-ttu-id="c0009-117">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="c0009-117">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="c0009-118">メッセージは削除対象としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="c0009-118">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="c0009-119">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="c0009-119">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="c0009-120">メッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="c0009-120">The message is not to be displayed.</span></span> 
    
<span data-ttu-id="c0009-121">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="c0009-121">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="c0009-122">メッセージは強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0009-122">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="c0009-123">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="c0009-123">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="c0009-124">メッセージがリモートメッセージストアで削除対象としてマークされ、ローカルクライアントにダウンロードされていません。</span><span class="sxs-lookup"><span data-stu-id="c0009-124">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="c0009-125">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="c0009-125">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="c0009-126">メッセージは、リモートメッセージストアからローカルクライアントにダウンロードするようにマークされています。</span><span class="sxs-lookup"><span data-stu-id="c0009-126">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="c0009-127">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="c0009-127">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="c0009-128">メッセージには、クライアント定義の目的のタグが付けられています。</span><span class="sxs-lookup"><span data-stu-id="c0009-128">The message has been tagged for a client-defined purpose.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c0009-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="c0009-129">Return value</span></span>

<span data-ttu-id="c0009-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0009-130">S_OK</span></span> 
  
> <span data-ttu-id="c0009-131">メッセージの状態が正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="c0009-131">The message status was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c0009-132">注釈</span><span class="sxs-lookup"><span data-stu-id="c0009-132">Remarks</span></span>

<span data-ttu-id="c0009-133">**imapifolder:: getmessagestatus**メソッドは、メッセージの状態を返します。</span><span class="sxs-lookup"><span data-stu-id="c0009-133">The **IMAPIFolder::GetMessageStatus** method returns the status of a message.</span></span> <span data-ttu-id="c0009-134">メッセージの状態は、メッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティに格納されます。</span><span class="sxs-lookup"><span data-stu-id="c0009-134">Message status is stored in the message's **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c0009-135">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="c0009-135">Notes to implementers</span></span>

<span data-ttu-id="c0009-136">メッセージ状態のビットがどのように設定、クリア、使用されるかは、実装に完全に依存します。ただし、ビット 0 ~ 15 は予約されており、0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0009-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> <span data-ttu-id="c0009-137">メッセージを ipm サブツリーに格納する場合、MAPI は、ipm クライアントによって使用されるビット 16 ~ 31 を予約します。</span><span class="sxs-lookup"><span data-stu-id="c0009-137">If you store messages in the IPM subtree, MAPI reserves bits 16 through 31 for use by IPM clients.</span></span> <span data-ttu-id="c0009-138">他のサブツリーにメッセージを格納する場合は、独自の用途にビット16から31を使用できます。</span><span class="sxs-lookup"><span data-stu-id="c0009-138">If you store messages in other subtrees, you can use bits 16 through 31 for your own purposes.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c0009-139">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="c0009-139">MFCMAPI reference</span></span>

<span data-ttu-id="c0009-140">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0009-140">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c0009-141">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="c0009-141">**File**</span></span>|<span data-ttu-id="c0009-142">**関数**</span><span class="sxs-lookup"><span data-stu-id="c0009-142">**Function**</span></span>|<span data-ttu-id="c0009-143">**コメント**</span><span class="sxs-lookup"><span data-stu-id="c0009-143">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c0009-144">MyMAPIFormViewer</span><span class="sxs-lookup"><span data-stu-id="c0009-144">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c0009-145">cmymapiformviewer:: GetNextMessage</span><span class="sxs-lookup"><span data-stu-id="c0009-145">CMyMAPIFormViewer::GetNextMessage</span></span>  <br/> |<span data-ttu-id="c0009-146">mfcmapi は、 **imapifolder:: getmessagestatus**メソッドを使用して、次に表示されるメッセージの状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="c0009-146">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the next message to be displayed.</span></span>  <br/> |
|<span data-ttu-id="c0009-147">MAPIFormFunctions</span><span class="sxs-lookup"><span data-stu-id="c0009-147">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c0009-148">openmessagenonmodal および openmessagemodal</span><span class="sxs-lookup"><span data-stu-id="c0009-148">OpenMessageNonModal and OpenMessageModal</span></span>  <br/> |<span data-ttu-id="c0009-149">mfcmapi は、 **imapifolder:: getmessagestatus**メソッドを使用して、フォームビューアーに渡すために表示されるメッセージの状態を取得します。これは、cmymapiformviewer または[imapifolder:: showform](imapisession-showform.md)のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="c0009-149">MFCMAPI uses the **IMAPIFolder::GetMessageStatus** method to get the status of the message to be displayed to pass to the form viewer, which is either CMyMAPIFormViewer or [IMAPISession::ShowForm](imapisession-showform.md).</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0009-150">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0009-150">See also</span></span>



[<span data-ttu-id="c0009-151">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="c0009-151">IMAPIFolder::SetMessageStatus</span></span>](imapifolder-setmessagestatus.md)
  
[<span data-ttu-id="c0009-152">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="c0009-152">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="c0009-153">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="c0009-153">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="c0009-154">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c0009-154">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


<span data-ttu-id="c0009-155">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="c0009-155">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

