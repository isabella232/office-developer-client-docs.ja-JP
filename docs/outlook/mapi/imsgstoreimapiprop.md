---
title: IMsgStore IMAPIProp
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422328"
---
# <a name="imsgstore--imapiprop"></a><span data-ttu-id="aa2c7-103">IMsgStore : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="aa2c7-103">IMsgStore : IMAPIProp</span></span>

  
  
<span data-ttu-id="aa2c7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa2c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa2c7-105">メッセージ ストア情報とメッセージとフォルダーへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-105">Provides access to message store information and to messages and folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aa2c7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="aa2c7-106">Header file:</span></span>  <br/> |<span data-ttu-id="aa2c7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aa2c7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="aa2c7-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="aa2c7-109">メッセージ ストア オブジェクト</span><span class="sxs-lookup"><span data-stu-id="aa2c7-109">Message store object</span></span>  <br/> |
|<span data-ttu-id="aa2c7-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="aa2c7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa2c7-111">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="aa2c7-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="aa2c7-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="aa2c7-112">Called by:</span></span>  <br/> |<span data-ttu-id="aa2c7-113">クライアント アプリケーション、MAPI スプーラー、MAPI</span><span class="sxs-lookup"><span data-stu-id="aa2c7-113">Client applications, the MAPI spooler, and MAPI</span></span>  <br/> |
|<span data-ttu-id="aa2c7-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="aa2c7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="aa2c7-115">IID_IMsgStore</span><span class="sxs-lookup"><span data-stu-id="aa2c7-115">IID_IMsgStore</span></span>  <br/> |
|<span data-ttu-id="aa2c7-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="aa2c7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="aa2c7-117">LPMDB</span><span class="sxs-lookup"><span data-stu-id="aa2c7-117">LPMDB</span></span>  <br/> |
|<span data-ttu-id="aa2c7-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="aa2c7-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="aa2c7-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="aa2c7-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="aa2c7-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="aa2c7-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="aa2c7-121">アドバイス</span><span class="sxs-lookup"><span data-stu-id="aa2c7-121">Advise</span></span>](imsgstore-advise.md) <br/> |<span data-ttu-id="aa2c7-122">メッセージ ストアに影響を与える指定されたイベントの通知を受信するために登録します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-122">Registers to receive notification of specified events that affect the message store.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-123">Unadvise</span><span class="sxs-lookup"><span data-stu-id="aa2c7-123">Unadvise</span></span>](imsgstore-unadvise.md) <br/> |<span data-ttu-id="aa2c7-124">**IMsgStore::Advise** メソッドへの呼び出しで以前に設定された通知の送信をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-124">Cancels the sending of notifications previously set up with a call to the **IMsgStore::Advise** method.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-125">CompareEntryIDs</span><span class="sxs-lookup"><span data-stu-id="aa2c7-125">CompareEntryIDs</span></span>](imsgstore-compareentryids.md) <br/> |<span data-ttu-id="aa2c7-126">2 つのエントリ識別子を比較して、メッセージ ストア内の同じエントリを参照するかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-126">Compares two entry identifiers to determine whether they refer to the same entry in a message store.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-127">OpenEntry</span><span class="sxs-lookup"><span data-stu-id="aa2c7-127">OpenEntry</span></span>](imsgstore-openentry.md) <br/> |<span data-ttu-id="aa2c7-128">フォルダーまたはメッセージを開き、さらにアクセスするインターフェイス ポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-128">Opens a folder or message and returns an interface pointer for further access.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-129">SetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="aa2c7-129">SetReceiveFolder</span></span>](imsgstore-setreceivefolder.md) <br/> |<span data-ttu-id="aa2c7-130">特定のメッセージ クラスの受信メッセージの宛先としてフォルダーを確立します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-130">Establishes a folder as the destination for incoming messages of a particular message class.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-131">GetReceiveFolder</span><span class="sxs-lookup"><span data-stu-id="aa2c7-131">GetReceiveFolder</span></span>](imsgstore-getreceivefolder.md) <br/> |<span data-ttu-id="aa2c7-132">指定したメッセージ クラスの受信メッセージの送信先として、またはメッセージ ストアの既定の受信フォルダーとして確立されたフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-132">Obtains the folder that was established as the destination for incoming messages of a specified message class or as the default receive folder for the message store.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-133">GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="aa2c7-133">GetReceiveFolderTable</span></span>](imsgstore-getreceivefoldertable.md) <br/> |<span data-ttu-id="aa2c7-134">メッセージ ストアのすべての受信フォルダーに関する情報を含む、受信フォルダー テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-134">Provides access to the receive folder table, a table with information about all of the receive folders for the message store.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-135">StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="aa2c7-135">StoreLogoff</span></span>](imsgstore-storelogoff.md) <br/> |<span data-ttu-id="aa2c7-136">メッセージ ストアの順序付けされたログオフを有効にします。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-136">Enables the orderly logoff of the message store.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-137">AbortSubmit</span><span class="sxs-lookup"><span data-stu-id="aa2c7-137">AbortSubmit</span></span>](imsgstore-abortsubmit.md) <br/> |<span data-ttu-id="aa2c7-138">送信キューからメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-138">Attempts to remove a message from the outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-139">GetOutgoingQueue</span><span class="sxs-lookup"><span data-stu-id="aa2c7-139">GetOutgoingQueue</span></span>](imsgstore-getoutgoingqueue.md) <br/> |<span data-ttu-id="aa2c7-140">メッセージ ストアの送信キュー内のすべてのメッセージに関する情報を含む、送信キュー テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-140">Provides access to the outgoing queue table, a table that has information about all of the messages in the message store's outgoing queue.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-141">SetLockState</span><span class="sxs-lookup"><span data-stu-id="aa2c7-141">SetLockState</span></span>](imsgstore-setlockstate.md) <br/> |<span data-ttu-id="aa2c7-142">メッセージをロックまたはロック解除します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-142">Locks or unlocks a message.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-143">FinishedMsg</span><span class="sxs-lookup"><span data-stu-id="aa2c7-143">FinishedMsg</span></span>](imsgstore-finishedmsg.md) <br/> |<span data-ttu-id="aa2c7-144">メッセージ ストア プロバイダーが送信されたメッセージに対して処理を実行できます。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-144">Enables the message store provider to perform processing on a sent message.</span></span>  <br/> |
|[<span data-ttu-id="aa2c7-145">NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="aa2c7-145">NotifyNewMail</span></span>](imsgstore-notifynewmail.md) <br/> |<span data-ttu-id="aa2c7-146">新しいメッセージが到着したとメッセージ ストアに通知します。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-146">Informs the message store that a new message has arrived.</span></span>  <br/> |
   
|<span data-ttu-id="aa2c7-147">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="aa2c7-147">**Required properties**</span></span>|<span data-ttu-id="aa2c7-148">**アクセス レベル**</span><span class="sxs-lookup"><span data-stu-id="aa2c7-148">**Access level**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aa2c7-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-149">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa2c7-150">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="aa2c7-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="aa2c7-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-151">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa2c7-152">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="aa2c7-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="aa2c7-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-153">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa2c7-154">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="aa2c7-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="aa2c7-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa2c7-156">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="aa2c7-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="aa2c7-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa2c7-158">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="aa2c7-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="aa2c7-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa2c7-160">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="aa2c7-160">Read-only</span></span>  <br/> |
|<span data-ttu-id="aa2c7-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-161">**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa2c7-162">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="aa2c7-162">Read-only</span></span>  <br/> |
|<span data-ttu-id="aa2c7-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-163">**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="aa2c7-164">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="aa2c7-164">Read-only</span></span>  <br/> |
   
<span data-ttu-id="aa2c7-165">次のプロパティは、対人間メッセージ (IPM) メッセージ ストア用です。</span><span class="sxs-lookup"><span data-stu-id="aa2c7-165">The following properties are for interpersonal message (IPM) message stores:</span></span>
  
- <span data-ttu-id="aa2c7-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-166">**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="aa2c7-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-167">**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="aa2c7-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-168">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="aa2c7-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="aa2c7-169">**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="aa2c7-170">**PR_MDB_PROVIDER**</span><span class="sxs-lookup"><span data-stu-id="aa2c7-170">**PR_MDB_PROVIDER**</span></span>
    
- <span data-ttu-id="aa2c7-171">**PR_STORE_SUPPORT_MASK**</span><span class="sxs-lookup"><span data-stu-id="aa2c7-171">**PR_STORE_SUPPORT_MASK**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aa2c7-172">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa2c7-172">See also</span></span>



[<span data-ttu-id="aa2c7-173">MAPI のプロパティ</span><span class="sxs-lookup"><span data-stu-id="aa2c7-173">MAPI Properties</span></span>](mapi-properties.md)

