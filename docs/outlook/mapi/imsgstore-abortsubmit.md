---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414383"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="ccb79-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="ccb79-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="ccb79-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccb79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccb79-105">送信キューからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="ccb79-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ccb79-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ccb79-106">Parameters</span></span>

 <span data-ttu-id="ccb79-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="ccb79-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="ccb79-108">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="ccb79-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="ccb79-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="ccb79-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="ccb79-110">[in]送信キューから削除するメッセージのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ccb79-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="ccb79-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ccb79-111">_ulFlags_</span></span>
  
> <span data-ttu-id="ccb79-112">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="ccb79-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ccb79-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="ccb79-113">Return value</span></span>

<span data-ttu-id="ccb79-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccb79-114">S_OK</span></span> 
  
> <span data-ttu-id="ccb79-115">メッセージが送信キューから正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="ccb79-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="ccb79-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="ccb79-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="ccb79-117">_lpEntryID_ によって識別されるメッセージは、メッセージ ストアの送信キューに存在しなくなりました。通常は、送信済みのためです。</span><span class="sxs-lookup"><span data-stu-id="ccb79-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="ccb79-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="ccb79-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="ccb79-119">_lpEntryID_ によって識別されるメッセージは、MAPI スプーラーによってロックされ、操作を中止することはできません。</span><span class="sxs-lookup"><span data-stu-id="ccb79-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ccb79-120">注釈</span><span class="sxs-lookup"><span data-stu-id="ccb79-120">Remarks</span></span>

<span data-ttu-id="ccb79-121">**IMsgStore::AbortSubmit** メソッドは、送信されたメッセージをメッセージ ストアの送信キューから削除します。</span><span class="sxs-lookup"><span data-stu-id="ccb79-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ccb79-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ccb79-122">Notes to callers</span></span>

<span data-ttu-id="ccb79-123">メッセージが送信された後 **、AbortSubmit** を呼び出して送信を中止する操作は、メッセージに対して実行できる唯一のアクションです。</span><span class="sxs-lookup"><span data-stu-id="ccb79-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="ccb79-124">**AbortSubmit** が常に成功するとは予想しません。</span><span class="sxs-lookup"><span data-stu-id="ccb79-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="ccb79-125">基になるメッセージング システムの実装方法によっては、メッセージの送信をキャンセルできない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ccb79-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ccb79-126">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="ccb79-126">MFCMAPI reference</span></span>

<span data-ttu-id="ccb79-127">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccb79-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ccb79-128">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="ccb79-128">**File**</span></span>|<span data-ttu-id="ccb79-129">**関数**</span><span class="sxs-lookup"><span data-stu-id="ccb79-129">**Function**</span></span>|<span data-ttu-id="ccb79-130">**コメント**</span><span class="sxs-lookup"><span data-stu-id="ccb79-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ccb79-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ccb79-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="ccb79-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="ccb79-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="ccb79-133">MFCMAPI は **、IMsgStore::AbortSubmit** メソッドを使用して、選択したメッセージの送信を中止します。</span><span class="sxs-lookup"><span data-stu-id="ccb79-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccb79-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="ccb79-134">See also</span></span>



[<span data-ttu-id="ccb79-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="ccb79-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="ccb79-136">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ccb79-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="ccb79-137">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ccb79-137">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

