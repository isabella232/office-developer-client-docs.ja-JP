---
title: IMsgStore imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348721"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="adce2-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="adce2-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="adce2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="adce2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="adce2-105">メッセージストア情報およびメッセージとフォルダーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="adce2-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="adce2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="adce2-106">Header file:</span></span>  <br/> |<span data-ttu-id="adce2-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="adce2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="adce2-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="adce2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="adce2-109">メッセージストアオブジェクト</span><span class="sxs-lookup"><span data-stu-id="adce2-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="adce2-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="adce2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="adce2-111">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="adce2-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="adce2-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="adce2-112">Called by:</span></span>  <br/> |<span data-ttu-id="adce2-113">クライアントアプリケーション、mapi スプーラー、mapi</span><span class="sxs-lookup"><span data-stu-id="adce2-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="adce2-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="adce2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="adce2-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="adce2-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="adce2-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="adce2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="adce2-117">lpmdb</span><span class="sxs-lookup"><span data-stu-id="adce2-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="adce2-118">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="adce2-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="adce2-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="adce2-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="adce2-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="adce2-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="adce2-121">助言</span><span class="sxs-lookup"><span data-stu-id="adce2-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="adce2-122">メッセージストアに影響を与える指定したイベントの通知を受信するように登録します。</span><span class="sxs-lookup"><span data-stu-id="adce2-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="adce2-123">アドバイズ</span><span class="sxs-lookup"><span data-stu-id="adce2-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="adce2-124">**IMsgStore:: Advise**メソッドへの呼び出しによって、以前に設定された通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="adce2-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="adce2-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="adce2-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="adce2-126">2つのエントリ識別子を比較して、メッセージストア内の同じエントリを参照しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="adce2-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="adce2-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="adce2-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="adce2-128">フォルダーまたはメッセージを開き、さらにアクセスするためのインターフェイスポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="adce2-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="adce2-129">setreceivefolder</span><span class="sxs-lookup"><span data-stu-id="adce2-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="adce2-130">特定のメッセージクラスの受信メッセージの送信先としてフォルダーを確立します。</span><span class="sxs-lookup"><span data-stu-id="adce2-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="adce2-131">getreceivefolder</span><span class="sxs-lookup"><span data-stu-id="adce2-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="adce2-132">指定したメッセージクラスの受信メッセージの宛先として、またはメッセージストアの既定の受信フォルダーとして確立されたフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="adce2-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="adce2-133">getreceivefoldertable</span><span class="sxs-lookup"><span data-stu-id="adce2-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="adce2-134">受信フォルダーテーブル (メッセージストアのすべての受信フォルダーに関する情報を含む表) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="adce2-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="adce2-135">storelogoff</span><span class="sxs-lookup"><span data-stu-id="adce2-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="adce2-136">メッセージストアの正常なログオフを有効にします。</span><span class="sxs-lookup"><span data-stu-id="adce2-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="adce2-137">abortsubmit</span><span class="sxs-lookup"><span data-stu-id="adce2-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="adce2-138">送信キューからメッセージを削除しようとしています。</span><span class="sxs-lookup"><span data-stu-id="adce2-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="adce2-139">getoutgoingqueue</span><span class="sxs-lookup"><span data-stu-id="adce2-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="adce2-140">送信キューテーブル (メッセージストアの送信キューにあるすべてのメッセージに関する情報を含むテーブル) へのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="adce2-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="adce2-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="adce2-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="adce2-142">メッセージをロックまたはロック解除します。</span><span class="sxs-lookup"><span data-stu-id="adce2-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="adce2-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="adce2-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="adce2-144">メッセージストアプロバイダーが、送信されたメッセージに対して処理を実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="adce2-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="adce2-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="adce2-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="adce2-146">新しいメッセージが到着したことをメッセージストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="adce2-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="adce2-147">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="adce2-147">**Required properties**</span></span>|<span data-ttu-id="adce2-148">**アクセスレベル**</span><span class="sxs-lookup"><span data-stu-id="adce2-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="adce2-149">**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="adce2-150">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="adce2-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="adce2-151">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="adce2-152">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="adce2-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="adce2-153">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="adce2-154">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="adce2-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="adce2-155">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="adce2-156">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="adce2-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="adce2-157">**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="adce2-158">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="adce2-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="adce2-159">**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="adce2-160">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="adce2-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="adce2-161">**PR_MDB_PROVIDER**([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="adce2-162">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="adce2-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="adce2-163">**PR_STORE_SUPPORT_MASK**([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="adce2-164">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="adce2-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="adce2-165">次のプロパティは、個人間メッセージ (IPM) メッセージストアに対するものです。</span><span class="sxs-lookup"><span data-stu-id="adce2-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="adce2-166">**PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="adce2-167">**PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="adce2-168">**PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="adce2-169">**PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="adce2-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="adce2-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="adce2-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="adce2-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="adce2-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="adce2-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="adce2-172">See also</span></span>



[<span data-ttu-id="adce2-173">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="adce2-173">MAPI Properties</span></span>](mapi-properties.md)

