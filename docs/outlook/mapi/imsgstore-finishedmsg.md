---
title: IMsgStoreFinishedMsg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.FinishedMsg
api_type:
- COM
ms.assetid: c32493fa-aa42-485b-9ea4-f93b835906df
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8b15f12c9a7ac2041c895b935098f9681e4b3a3c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589953"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="a9422-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="a9422-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="a9422-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9422-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9422-105">メッセージ ストア プロバイダーは、送信されたメッセージの処理を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a9422-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="a9422-106">このメソッドは、MAPI スプーラーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a9422-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="a9422-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a9422-107">Parameters</span></span>

 <span data-ttu-id="a9422-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a9422-108">_ulFlags_</span></span>
  
> <span data-ttu-id="a9422-109">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a9422-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a9422-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a9422-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="a9422-111">[in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="a9422-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a9422-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="a9422-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="a9422-113">[in]処理されるメッセージのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a9422-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a9422-114">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a9422-114">Return value</span></span>

<span data-ttu-id="a9422-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9422-115">S_OK</span></span> 
  
> <span data-ttu-id="a9422-116">送信済みメッセージの処理が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="a9422-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="a9422-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="a9422-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="a9422-118">メッセージ ストア プロバイダーは、送信済みメッセージの処理をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="a9422-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="a9422-119">呼び出し元は、MAPI スプーラーではない場合、エラー値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a9422-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a9422-120">注釈</span><span class="sxs-lookup"><span data-stu-id="a9422-120">Remarks</span></span>

<span data-ttu-id="a9422-121">**IMsgStore::FinishedMsg**メソッドでは、送信されたメッセージの処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="a9422-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="a9422-122">この処理には、別のフォルダー、または両方のアクションに移動すること、メッセージの削除が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a9422-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="a9422-123">処理の種類は、 **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) と**PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) のプロパティを設定するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="a9422-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a9422-124">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="a9422-124">Notes to implementers</span></span>

<span data-ttu-id="a9422-125">実装では、 **FinishedMsg**の_lpEntryID_で識別されるメッセージのロックを解除し、適切な処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="a9422-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="a9422-126">移行先のメッセージは常にロックされます。MAPI スプーラーは、決して**FinishedMsg**にロックされていないメッセージのエントリ id を渡します。</span><span class="sxs-lookup"><span data-stu-id="a9422-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="a9422-127">**PR_DELETE_AFTER_SUBMIT**または**PR_SENTMAIL_ENTRYID**が設定されて、両方を設定するでもどちらか一方を設定します。</span><span class="sxs-lookup"><span data-stu-id="a9422-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="a9422-128">次の表には、設定に基づいて取るべきアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a9422-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9422-129">場合は 2 つのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9422-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="a9422-130">(通常、[送信トレイ]) の送信、元のフォルダーにメッセージを残します。</span><span class="sxs-lookup"><span data-stu-id="a9422-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="a9422-131">両方のプロパティが設定されます。 場合、</span><span class="sxs-lookup"><span data-stu-id="a9422-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="a9422-132">必要な場合にメッセージを指定されたフォルダーに移動し、そのパーティションを削除します。</span><span class="sxs-lookup"><span data-stu-id="a9422-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="a9422-133">場合は PR_SENTMAIL_ENTRYID が設定されます。</span><span class="sxs-lookup"><span data-stu-id="a9422-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="a9422-134">指定されたフォルダーにメッセージを移動します。</span><span class="sxs-lookup"><span data-stu-id="a9422-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="a9422-135">場合は PR_DELETE_AFTER_SUBMIT が設定されます。</span><span class="sxs-lookup"><span data-stu-id="a9422-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="a9422-136">メッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="a9422-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="a9422-137">適切な処理を実行した後は、 [IMAPISupport::DoSentMail](imapisupport-dosentmail.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a9422-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9422-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="a9422-138">See also</span></span>



[<span data-ttu-id="a9422-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="a9422-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="a9422-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="a9422-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

