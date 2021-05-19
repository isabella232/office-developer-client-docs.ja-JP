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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424239"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="fce2a-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="fce2a-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="fce2a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fce2a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fce2a-105">フォルダー内のメッセージとサブフォルダーに対して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fce2a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fce2a-106">Header file:</span></span>  <br/> |<span data-ttu-id="fce2a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fce2a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="fce2a-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="fce2a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="fce2a-109">フォルダー オブジェクト</span><span class="sxs-lookup"><span data-stu-id="fce2a-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="fce2a-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="fce2a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="fce2a-111">メッセージ ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="fce2a-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="fce2a-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="fce2a-112">Called by:</span></span>  <br/> |<span data-ttu-id="fce2a-113">クライアント アプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="fce2a-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="fce2a-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="fce2a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fce2a-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="fce2a-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="fce2a-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="fce2a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="fce2a-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="fce2a-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="fce2a-118">トランザクション モデル:</span><span class="sxs-lookup"><span data-stu-id="fce2a-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="fce2a-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="fce2a-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fce2a-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="fce2a-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="fce2a-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="fce2a-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="fce2a-122">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-123">CopyMessages</span><span class="sxs-lookup"><span data-stu-id="fce2a-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="fce2a-124">1 つ以上のメッセージをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="fce2a-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="fce2a-126">1 つ以上のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="fce2a-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="fce2a-128">新しいサブフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="fce2a-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="fce2a-130">サブフォルダーをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="fce2a-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="fce2a-132">サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-133">SetReadFlags</span><span class="sxs-lookup"><span data-stu-id="fce2a-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="fce2a-134">**1** つ以上のフォルダーのメッセージの PR_MESSAGE_FLAGS ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、読み取りレポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-135">GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="fce2a-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="fce2a-136">特定のフォルダー内のメッセージに関連付けられている状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-137">SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="fce2a-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="fce2a-138">メッセージに関連付けられた状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="fce2a-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="fce2a-140">フォルダーのコンテンツ テーブルの既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="fce2a-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="fce2a-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="fce2a-142">フォルダー自体を削除せずに、フォルダーからすべてのメッセージとサブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="fce2a-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="fce2a-143">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="fce2a-143">**Required properties**</span></span>|<span data-ttu-id="fce2a-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="fce2a-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fce2a-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce2a-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fce2a-146">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="fce2a-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="fce2a-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce2a-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fce2a-148">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="fce2a-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="fce2a-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce2a-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fce2a-150">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="fce2a-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="fce2a-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce2a-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fce2a-152">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="fce2a-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="fce2a-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce2a-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fce2a-154">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="fce2a-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="fce2a-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce2a-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fce2a-156">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="fce2a-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="fce2a-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce2a-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fce2a-158">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="fce2a-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="fce2a-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="fce2a-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="fce2a-160">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="fce2a-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fce2a-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="fce2a-161">See also</span></span>



[<span data-ttu-id="fce2a-162">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="fce2a-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

