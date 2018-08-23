---
title: IMAPIFolder IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder
api_type:
- COM
ms.assetid: bc2e8d17-7687-43c2-8f01-b677703f7288
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 64a64029c3507d9ac4b520076a44e23170dd9bd4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800508"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="975fd-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="975fd-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="975fd-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="975fd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="975fd-105">フォルダー内のメッセージとサブフォルダーに対して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="975fd-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="975fd-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="975fd-106">Header file:</span></span>  <br/> |<span data-ttu-id="975fd-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="975fd-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="975fd-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="975fd-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="975fd-109">フォルダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="975fd-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="975fd-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="975fd-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="975fd-111">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="975fd-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="975fd-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="975fd-112">Called by:</span></span>  <br/> |<span data-ttu-id="975fd-113">クライアント アプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="975fd-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="975fd-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="975fd-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="975fd-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="975fd-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="975fd-116">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="975fd-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="975fd-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="975fd-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="975fd-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="975fd-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="975fd-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="975fd-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="975fd-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="975fd-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="975fd-121">メイル</span><span class="sxs-lookup"><span data-stu-id="975fd-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="975fd-122">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="975fd-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="975fd-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="975fd-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="975fd-124">1 つまたは複数のメッセージを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="975fd-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="975fd-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="975fd-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="975fd-126">1 つまたは複数のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="975fd-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="975fd-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="975fd-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="975fd-128">新しいサブフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="975fd-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="975fd-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="975fd-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="975fd-130">サブフォルダーを移動またはコピーします。</span><span class="sxs-lookup"><span data-stu-id="975fd-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="975fd-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="975fd-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="975fd-132">サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="975fd-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="975fd-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="975fd-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="975fd-134">設定または、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティに 1 つまたは複数のフォルダーのメッセージでは、MSGFLAG_READ フラグをクリアし、リードのレポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="975fd-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="975fd-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="975fd-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="975fd-136">特定のフォルダー内のメッセージに関連付けられているステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="975fd-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="975fd-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="975fd-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="975fd-138">メッセージに関連付けられているステータスを設定します。</span><span class="sxs-lookup"><span data-stu-id="975fd-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="975fd-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="975fd-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="975fd-140">フォルダーの内容のテーブルの既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="975fd-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="975fd-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="975fd-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="975fd-142">フォルダー自体を削除することがなく、フォルダーからすべてのメッセージとサブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="975fd-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="975fd-143">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="975fd-143">**Required properties**</span></span>|<span data-ttu-id="975fd-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="975fd-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="975fd-145">**PR_DISPLAY_NAME**([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="975fd-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="975fd-146">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="975fd-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="975fd-147">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="975fd-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="975fd-148">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="975fd-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="975fd-149">**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="975fd-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="975fd-150">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="975fd-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="975fd-151">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="975fd-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="975fd-152">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="975fd-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="975fd-153">**PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="975fd-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="975fd-154">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="975fd-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="975fd-155">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="975fd-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="975fd-156">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="975fd-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="975fd-157">**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="975fd-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="975fd-158">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="975fd-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="975fd-159">**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="975fd-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="975fd-160">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="975fd-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="975fd-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="975fd-161">See also</span></span>



[<span data-ttu-id="975fd-162">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="975fd-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

