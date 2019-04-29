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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e31896354141999e02f2cba117ef9739340be61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424239"
---
# <a name="imapifolder--imapicontainer"></a><span data-ttu-id="eab67-103">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="eab67-103">IMAPIFolder : IMAPIContainer</span></span>

  
  
<span data-ttu-id="eab67-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eab67-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eab67-105">フォルダー内のメッセージとサブフォルダーに対して操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="eab67-105">Performs operations on the messages and subfolders in a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eab67-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="eab67-106">Header file:</span></span>  <br/> |<span data-ttu-id="eab67-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eab67-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="eab67-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="eab67-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="eab67-109">Folder オブジェクト</span><span class="sxs-lookup"><span data-stu-id="eab67-109">Folder objects</span></span>  <br/> |
|<span data-ttu-id="eab67-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="eab67-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="eab67-111">メッセージストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="eab67-111">Message store providers</span></span>  <br/> |
|<span data-ttu-id="eab67-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="eab67-112">Called by:</span></span>  <br/> |<span data-ttu-id="eab67-113">クライアントアプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="eab67-113">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="eab67-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="eab67-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eab67-115">IID_IMAPIFolder</span><span class="sxs-lookup"><span data-stu-id="eab67-115">IID_IMAPIFolder</span></span>  <br/> |
|<span data-ttu-id="eab67-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="eab67-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="eab67-117">LPMAPIFOLDER</span><span class="sxs-lookup"><span data-stu-id="eab67-117">LPMAPIFOLDER</span></span>  <br/> |
|<span data-ttu-id="eab67-118">トランザクションモデル:</span><span class="sxs-lookup"><span data-stu-id="eab67-118">Transaction model:</span></span>  <br/> |<span data-ttu-id="eab67-119">非トランザクション</span><span class="sxs-lookup"><span data-stu-id="eab67-119">Nontransacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="eab67-120">v の順序</span><span class="sxs-lookup"><span data-stu-id="eab67-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="eab67-121">CreateMessage</span><span class="sxs-lookup"><span data-stu-id="eab67-121">CreateMessage</span></span>](imapifolder-createmessage.md) <br/> |<span data-ttu-id="eab67-122">新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="eab67-122">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="eab67-123">copymessages</span><span class="sxs-lookup"><span data-stu-id="eab67-123">CopyMessages</span></span>](imapifolder-copymessages.md) <br/> |<span data-ttu-id="eab67-124">1つまたは複数のメッセージをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="eab67-124">Copies or moves one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="eab67-125">DeleteMessages</span><span class="sxs-lookup"><span data-stu-id="eab67-125">DeleteMessages</span></span>](imapifolder-deletemessages.md) <br/> |<span data-ttu-id="eab67-126">1つまたは複数のメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="eab67-126">Deletes one or more messages.</span></span>  <br/> |
|[<span data-ttu-id="eab67-127">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="eab67-127">CreateFolder</span></span>](imapifolder-createfolder.md) <br/> |<span data-ttu-id="eab67-128">新しいサブフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="eab67-128">Creates a new subfolder.</span></span>  <br/> |
|[<span data-ttu-id="eab67-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="eab67-129">CopyFolder</span></span>](imapifolder-copyfolder.md) <br/> |<span data-ttu-id="eab67-130">サブフォルダーをコピーまたは移動します。</span><span class="sxs-lookup"><span data-stu-id="eab67-130">Copies or moves a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="eab67-131">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="eab67-131">DeleteFolder</span></span>](imapifolder-deletefolder.md) <br/> |<span data-ttu-id="eab67-132">サブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="eab67-132">Deletes a subfolder.</span></span>  <br/> |
|[<span data-ttu-id="eab67-133">setreadflags</span><span class="sxs-lookup"><span data-stu-id="eab67-133">SetReadFlags</span></span>](imapifolder-setreadflags.md) <br/> |<span data-ttu-id="eab67-134">1つ以上のフォルダーのメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティの MSGFLAG_READ フラグを設定またはクリアし、閲覧レポートの送信を管理します。</span><span class="sxs-lookup"><span data-stu-id="eab67-134">Sets or clears the MSGFLAG_READ flag in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of one or more of the folder's messages, and manages the sending of read reports.</span></span>  <br/> |
|[<span data-ttu-id="eab67-135">getmessagestatus</span><span class="sxs-lookup"><span data-stu-id="eab67-135">GetMessageStatus</span></span>](imapifolder-getmessagestatus.md) <br/> |<span data-ttu-id="eab67-136">特定のフォルダー内のメッセージに関連付けられている状態を取得します。</span><span class="sxs-lookup"><span data-stu-id="eab67-136">Obtains the status associated with a message in a particular folder.</span></span>  <br/> |
|[<span data-ttu-id="eab67-137">setmessagestatus</span><span class="sxs-lookup"><span data-stu-id="eab67-137">SetMessageStatus</span></span>](imapifolder-setmessagestatus.md) <br/> |<span data-ttu-id="eab67-138">メッセージに関連付けられている状態を設定します。</span><span class="sxs-lookup"><span data-stu-id="eab67-138">Sets the status associated with a message.</span></span>  <br/> |
|[<span data-ttu-id="eab67-139">SaveContentsSort</span><span class="sxs-lookup"><span data-stu-id="eab67-139">SaveContentsSort</span></span>](imapifolder-savecontentssort.md) <br/> |<span data-ttu-id="eab67-140">フォルダーの contents テーブルの既定の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="eab67-140">Sets the default sort order for a folder's contents table.</span></span>  <br/> |
|[<span data-ttu-id="eab67-141">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="eab67-141">EmptyFolder</span></span>](imapifolder-emptyfolder.md) <br/> |<span data-ttu-id="eab67-142">フォルダー自体を削除せずに、フォルダーからすべてのメッセージとサブフォルダーを削除します。</span><span class="sxs-lookup"><span data-stu-id="eab67-142">Deletes all messages and subfolders from a folder without deleting the folder itself.</span></span>  <br/> |
   
|<span data-ttu-id="eab67-143">**必須のプロパティ**</span><span class="sxs-lookup"><span data-stu-id="eab67-143">**Required properties**</span></span>|<span data-ttu-id="eab67-144">**Access**</span><span class="sxs-lookup"><span data-stu-id="eab67-144">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="eab67-145">**PR_DISPLAY_NAME**([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eab67-145">**PR_DISPLAY_NAME** ([PidTagDisplayNamePrefix](pidtagdisplaynameprefix-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eab67-146">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="eab67-146">Read/write</span></span>  <br/> |
|<span data-ttu-id="eab67-147">**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eab67-147">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eab67-148">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="eab67-148">Read-only</span></span>  <br/> |
|<span data-ttu-id="eab67-149">**PR_FOLDER_TYPE**([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eab67-149">**PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eab67-150">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="eab67-150">Read/write</span></span>  <br/> |
|<span data-ttu-id="eab67-151">**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eab67-151">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eab67-152">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="eab67-152">Read-only</span></span>  <br/> |
|<span data-ttu-id="eab67-153">**PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eab67-153">**PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eab67-154">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="eab67-154">Read-only</span></span>  <br/> |
|<span data-ttu-id="eab67-155">**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eab67-155">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eab67-156">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="eab67-156">Read-only</span></span>  <br/> |
|<span data-ttu-id="eab67-157">**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eab67-157">**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eab67-158">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="eab67-158">Read-only</span></span>  <br/> |
|<span data-ttu-id="eab67-159">**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="eab67-159">**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="eab67-160">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="eab67-160">Read-only</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eab67-161">関連項目</span><span class="sxs-lookup"><span data-stu-id="eab67-161">See also</span></span>



[<span data-ttu-id="eab67-162">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="eab67-162">MAPI Interfaces</span></span>](mapi-interfaces.md)

