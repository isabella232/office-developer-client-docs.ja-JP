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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e2871f5804cda172328fbd3ebdc43f860de939ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801007"
---
# <a name="imsgstoreabortsubmit"></a><span data-ttu-id="31a70-103">IMsgStore::AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="31a70-103">IMsgStore::AbortSubmit</span></span>

  
  
<span data-ttu-id="31a70-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31a70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31a70-105">発信キューからメッセージを削除しようとしています。</span><span class="sxs-lookup"><span data-stu-id="31a70-105">Attempts to remove a message from the outgoing queue.</span></span>
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="31a70-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="31a70-106">Parameters</span></span>

 <span data-ttu-id="31a70-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="31a70-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="31a70-108">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="31a70-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="31a70-109">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="31a70-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="31a70-110">[in]発信キューから削除するメッセージのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="31a70-110">[in] A pointer to the entry identifier of the message to remove from the outgoing queue.</span></span> 
    
 <span data-ttu-id="31a70-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="31a70-111">_ulFlags_</span></span>
  
> <span data-ttu-id="31a70-112">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="31a70-112">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31a70-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="31a70-113">Return value</span></span>

<span data-ttu-id="31a70-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="31a70-114">S_OK</span></span> 
  
> <span data-ttu-id="31a70-115">メッセージは発信キューから正常に削除されました。</span><span class="sxs-lookup"><span data-stu-id="31a70-115">The message was successfully removed from the outgoing queue.</span></span>
    
<span data-ttu-id="31a70-116">MAPI_E_NOT_IN_QUEUE</span><span class="sxs-lookup"><span data-stu-id="31a70-116">MAPI_E_NOT_IN_QUEUE</span></span> 
  
> <span data-ttu-id="31a70-117">_LpEntryID_によって識別されるメッセージはありません、メッセージ ストアの送信キューに通常既に送信されています。</span><span class="sxs-lookup"><span data-stu-id="31a70-117">The message identified by  _lpEntryID_ is no longer in the message store's outgoing queue, typically because it has already been sent.</span></span> 
    
<span data-ttu-id="31a70-118">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="31a70-118">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="31a70-119">_LpEntryID_によって識別されるメッセージは、MAPI スプーラーによってロックされているし、操作は中止できません。</span><span class="sxs-lookup"><span data-stu-id="31a70-119">The message identified by  _lpEntryID_ is locked by the MAPI spooler, and the operation cannot be aborted.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31a70-120">注釈</span><span class="sxs-lookup"><span data-stu-id="31a70-120">Remarks</span></span>

<span data-ttu-id="31a70-121">**IMsgStore::AbortSubmit**メソッドは、メッセージ ストアの送信キューから送信されたメッセージを削除しようとします。</span><span class="sxs-lookup"><span data-stu-id="31a70-121">The **IMsgStore::AbortSubmit** method attempts to remove a submitted message from the message store's outgoing queue.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="31a70-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="31a70-122">Notes to callers</span></span>

<span data-ttu-id="31a70-123">メッセージが送信されると、メッセージに対して実行できる操作だけでは**AbortSubmit**を呼び出すことによって、送信を中止しています。</span><span class="sxs-lookup"><span data-stu-id="31a70-123">After a message is submitted, aborting the submission by calling **AbortSubmit** is the only action that can be performed on the message.</span></span> <span data-ttu-id="31a70-124">常に成功するために**AbortSubmit**は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="31a70-124">Do not expect **AbortSubmit** to always succeed.</span></span> <span data-ttu-id="31a70-125">基になるメッセージング システムの実装方法によっては、できない可能性がありますメッセージの送信を中止します。</span><span class="sxs-lookup"><span data-stu-id="31a70-125">Depending on how the underlying messaging system is implemented, it might not be possible to cancel the sending of the message.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="31a70-126">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="31a70-126">MFCMAPI reference</span></span>

<span data-ttu-id="31a70-127">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="31a70-127">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="31a70-128">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="31a70-128">**File**</span></span>|<span data-ttu-id="31a70-129">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="31a70-129">**Function**</span></span>|<span data-ttu-id="31a70-130">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="31a70-130">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="31a70-131">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="31a70-131">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="31a70-132">CFolderDlg::OnAbortSubmit</span><span class="sxs-lookup"><span data-stu-id="31a70-132">CFolderDlg::OnAbortSubmit</span></span>  <br/> |<span data-ttu-id="31a70-133">MFCMAPI では、 **IMsgStore::AbortSubmit**メソッドを使用して、選択したメッセージの送信を中止します。</span><span class="sxs-lookup"><span data-stu-id="31a70-133">MFCMAPI uses the **IMsgStore::AbortSubmit** method to abort the submission of the selected message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31a70-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="31a70-134">See also</span></span>



[<span data-ttu-id="31a70-135">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="31a70-135">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="31a70-136">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="31a70-136">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


<span data-ttu-id="31a70-137">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="31a70-137">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

