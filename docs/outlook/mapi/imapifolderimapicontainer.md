---
title: imapifolder IMAPIContainer
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
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329492"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="f29b3-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f29b3-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="f29b3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f29b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f29b3-105">フォルダー内のメッセージとサブフォルダーに対して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f29b3-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f29b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="f29b3-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f29b3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f29b3-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="f29b3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f29b3-109">Folder オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f29b3-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="f29b3-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="f29b3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f29b3-111">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="f29b3-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="f29b3-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f29b3-112">Called by:</span></span>  <br/> |<span data-ttu-id="f29b3-113">クライアントアプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="f29b3-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="f29b3-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="f29b3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f29b3-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="f29b3-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="f29b3-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="f29b3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f29b3-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="f29b3-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="f29b3-118">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="f29b3-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="f29b3-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="f29b3-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f29b3-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="f29b3-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f29b3-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="f29b3-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="f29b3-122">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-123">copymessages</span><span class="sxs-lookup"><span data-stu-id="f29b3-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="f29b3-124">1つまたは複数のメッセージをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="f29b3-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="f29b3-126">1つまたは複数のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="f29b3-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="f29b3-128">新しいサブフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="f29b3-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="f29b3-130">サブフォルダーをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="f29b3-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="f29b3-132">サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-133">setreadflags</span><span class="sxs-lookup"><span data-stu-id="f29b3-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="f29b3-134">1つ以上のフォルダーのメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、閲覧レポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-135">getmessagestatus</span><span class="sxs-lookup"><span data-stu-id="f29b3-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="f29b3-136">特定のフォルダー内のメッセージに関連付けられている状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-137">setmessagestatus</span><span class="sxs-lookup"><span data-stu-id="f29b3-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="f29b3-138">メッセージに関連付けられている状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="f29b3-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="f29b3-140">フォルダーの contents テーブルの既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="f29b3-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="f29b3-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="f29b3-142">フォルダー自体を削除せずに、フォルダーからすべてのメッセージとサブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="f29b3-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="f29b3-143">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="f29b3-143">**Required properties**</span></span>|<span data-ttu-id="f29b3-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="f29b3-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f29b3-145">**PR_DISPLAY_NAME**([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f29b3-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f29b3-146">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="f29b3-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="f29b3-147">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f29b3-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f29b3-148">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f29b3-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="f29b3-149">**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f29b3-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f29b3-150">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="f29b3-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="f29b3-151">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f29b3-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f29b3-152">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f29b3-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="f29b3-153">**PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f29b3-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f29b3-154">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f29b3-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="f29b3-155">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f29b3-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f29b3-156">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f29b3-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="f29b3-157">**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f29b3-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f29b3-158">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f29b3-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="f29b3-159">**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f29b3-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f29b3-160">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="f29b3-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f29b3-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="f29b3-161">See also</span></span>



[<span data-ttu-id="f29b3-162">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="f29b3-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

