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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e7d7ba91791258eca93a2b8bedf95cf121062c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427088"
---
# <a name="imsgstorefinishedmsg"></a><span data-ttu-id="84a60-103">IMsgStore::FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="84a60-103">IMsgStore::FinishedMsg</span></span>

  
  
<span data-ttu-id="84a60-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84a60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84a60-105">メッセージ ストア プロバイダーが送信されたメッセージに対して処理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="84a60-105">Enables the message store provider to perform processing on a sent message.</span></span> <span data-ttu-id="84a60-106">このメソッドは、MAPI スプーラーによってのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84a60-106">This method is called only by the MAPI spooler.</span></span>
  
```cpp
HRESULT FinishedMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="84a60-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a60-107">Parameters</span></span>

 <span data-ttu-id="84a60-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="84a60-108">_ulFlags_</span></span>
  
> <span data-ttu-id="84a60-109">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="84a60-109">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="84a60-110">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="84a60-110">_cbEntryID_</span></span>
  
> <span data-ttu-id="84a60-111">[in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="84a60-111">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="84a60-112">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="84a60-112">_lpEntryID_</span></span>
  
> <span data-ttu-id="84a60-113">[in]処理するメッセージのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="84a60-113">[in] A pointer to the entry identifier of the message to be processed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84a60-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a60-114">Return value</span></span>

<span data-ttu-id="84a60-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="84a60-115">S_OK</span></span> 
  
> <span data-ttu-id="84a60-116">送信されたメッセージの処理が成功しました。</span><span class="sxs-lookup"><span data-stu-id="84a60-116">Processing on the sent message was successful.</span></span>
    
<span data-ttu-id="84a60-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="84a60-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="84a60-118">メッセージ ストア プロバイダーは、送信されたメッセージ処理をサポートしていない。</span><span class="sxs-lookup"><span data-stu-id="84a60-118">The message store provider does not support sent message processing.</span></span> <span data-ttu-id="84a60-119">呼び出し元が MAPI スプーラーではない場合、このエラー値が返されます。</span><span class="sxs-lookup"><span data-stu-id="84a60-119">This error value is returned if the caller is not the MAPI spooler.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84a60-120">注釈</span><span class="sxs-lookup"><span data-stu-id="84a60-120">Remarks</span></span>

<span data-ttu-id="84a60-121">**IMsgStore::FinishedMsg** メソッドは、送信されたメッセージに対して処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="84a60-121">The **IMsgStore::FinishedMsg** method performs processing on a sent message.</span></span> <span data-ttu-id="84a60-122">この処理には、メッセージの削除、別のフォルダーへの移動、または両方のアクションが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="84a60-122">This processing can involve deleting the message, moving it to a different folder, or both actions.</span></span> <span data-ttu-id="84a60-123">処理の種類は **、PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) プロパティと **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) プロパティが設定されるかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="84a60-123">The type of processing depends on whether the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) and **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) properties are set.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="84a60-124">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="84a60-124">Notes to implementers</span></span>

<span data-ttu-id="84a60-125">**FinishedMsg の実装で**_、lpEntryID_ によって識別されるメッセージのロックを解除し、適切な処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="84a60-125">In your implementation of **FinishedMsg**, unlock the message identified by  _lpEntryID_ and perform the appropriate processing.</span></span> <span data-ttu-id="84a60-126">ターゲット メッセージは常にロックされます。MAPI スプーラーは、ロックされていないメッセージのエントリ識別子を **FinishedMsg に渡す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="84a60-126">The target message will always be locked; the MAPI spooler never passes the entry identifier for an unlocked message to **FinishedMsg**.</span></span>
  
<span data-ttu-id="84a60-127">設定されているファイルまたは **PR_DELETE_AFTER_SUBMIT、PR_SENTMAIL_ENTRYID** 設定、または設定されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="84a60-127">It is possible that neither **PR_DELETE_AFTER_SUBMIT** or **PR_SENTMAIL_ENTRYID** is set, both are set, or one or the other is set.</span></span> <span data-ttu-id="84a60-128">次の表では、設定に基づいて実行する必要があるアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="84a60-128">The following table describes the action you should take based on the settings:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84a60-129">どちらのプロパティも設定しない場合:</span><span class="sxs-lookup"><span data-stu-id="84a60-129">If neither property is set:</span></span>  <br/> |<span data-ttu-id="84a60-130">メッセージは、送信されたフォルダー (通常は送信箱) に残します。</span><span class="sxs-lookup"><span data-stu-id="84a60-130">Leave the message in the folder from which it was sent (typically the Outbox).</span></span>  <br/> |
|<span data-ttu-id="84a60-131">両方のプロパティが設定されている場合:</span><span class="sxs-lookup"><span data-stu-id="84a60-131">If both properties are set:</span></span>  <br/> |<span data-ttu-id="84a60-132">必要に応じて、メッセージを指定したフォルダーに移動し、削除します。</span><span class="sxs-lookup"><span data-stu-id="84a60-132">Move the message to the indicated folder, if desired, and then delete it.</span></span>  <br/> |
|<span data-ttu-id="84a60-133">このPR_SENTMAIL_ENTRYID設定されている場合は、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="84a60-133">If PR_SENTMAIL_ENTRYID is set:</span></span>  <br/> |<span data-ttu-id="84a60-134">メッセージを指定したフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="84a60-134">Move the message to the indicated folder.</span></span>  <br/> |
|<span data-ttu-id="84a60-135">このPR_DELETE_AFTER_SUBMIT設定されている場合は、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="84a60-135">If PR_DELETE_AFTER_SUBMIT is set:</span></span>  <br/> |<span data-ttu-id="84a60-136">メッセージを削除する。</span><span class="sxs-lookup"><span data-stu-id="84a60-136">Delete the message.</span></span>  <br/> |
   
<span data-ttu-id="84a60-137">適切な操作を実行した後 [、IMAPISupport::D oSentMail メソッドを呼び出](imapisupport-dosentmail.md) します。</span><span class="sxs-lookup"><span data-stu-id="84a60-137">After you have taken whatever action is appropriate, call the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="84a60-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="84a60-138">See also</span></span>



[<span data-ttu-id="84a60-139">IMAPISupport::DoSentMail</span><span class="sxs-lookup"><span data-stu-id="84a60-139">IMAPISupport::DoSentMail</span></span>](imapisupport-dosentmail.md)
  
[<span data-ttu-id="84a60-140">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="84a60-140">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)

