---
title: imapifoldersetmessagestatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342778"
---
# <a name="imapifoldersetmessagestatus"></a><span data-ttu-id="a6b8d-103">IMAPIFolder::SetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="a6b8d-103">IMAPIFolder::SetMessageStatus</span></span>

  
  
<span data-ttu-id="a6b8d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6b8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6b8d-105">メッセージに関連付けられている状態を設定します (メッセージに削除のマークが付いているかどうかなど)。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-105">Sets the status associated with a message (for example, whether that message is marked for deletion).</span></span>
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a><span data-ttu-id="a6b8d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a6b8d-106">Parameters</span></span>

 <span data-ttu-id="a6b8d-107">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="a6b8d-107">_cbEntryID_</span></span>
  
> <span data-ttu-id="a6b8d-108">順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-108">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="a6b8d-109">_lて tryid_</span><span class="sxs-lookup"><span data-stu-id="a6b8d-109">_lpEntryID_</span></span>
  
> <span data-ttu-id="a6b8d-110">順番状態が設定されているメッセージのエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-110">[in] A pointer to the entry identifier for the message whose status is set.</span></span>
    
 <span data-ttu-id="a6b8d-111">_ulnewstatus_</span><span class="sxs-lookup"><span data-stu-id="a6b8d-111">_ulNewStatus_</span></span>
  
> <span data-ttu-id="a6b8d-112">順番割り当てられる新しい状態。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-112">[in] The new status to be assigned.</span></span> 
    
 <span data-ttu-id="a6b8d-113">_ulnewstatusmask_</span><span class="sxs-lookup"><span data-stu-id="a6b8d-113">_ulNewStatusMask_</span></span>
  
> <span data-ttu-id="a6b8d-114">順番新しい状態に適用されるフラグのビットマスク。設定するフラグを示します。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-114">[in] A bitmask of flags that is applied to the new status and indicates the flags to be set.</span></span> <span data-ttu-id="a6b8d-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-115">The following flags can be set:</span></span>
    
<span data-ttu-id="a6b8d-116">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="a6b8d-116">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="a6b8d-117">メッセージは削除対象としてマークされています。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-117">The message has been marked for deletion.</span></span>
    
<span data-ttu-id="a6b8d-118">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="a6b8d-118">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="a6b8d-119">メッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-119">The message is not to be displayed.</span></span>
    
<span data-ttu-id="a6b8d-120">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="a6b8d-120">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="a6b8d-121">メッセージは強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-121">The message is to be displayed highlighted.</span></span>
    
<span data-ttu-id="a6b8d-122">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="a6b8d-122">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="a6b8d-123">メッセージがリモートメッセージストアで削除対象としてマークされ、ローカルクライアントにダウンロードされていません。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-123">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span>
    
<span data-ttu-id="a6b8d-124">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="a6b8d-124">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="a6b8d-125">メッセージは、リモートメッセージストアからローカルクライアントにダウンロードするようにマークされています。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-125">The message has been marked for downloading from the remote message store to the local client.</span></span>
    
<span data-ttu-id="a6b8d-126">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="a6b8d-126">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="a6b8d-127">メッセージには、クライアント定義の目的のタグが付けられています。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-127">The message has been tagged for a client-defined purpose.</span></span>
    
 <span data-ttu-id="a6b8d-128">_lpuloldstatus_</span><span class="sxs-lookup"><span data-stu-id="a6b8d-128">_lpulOldStatus_</span></span>
  
> <span data-ttu-id="a6b8d-129">読み上げメッセージの以前の状態へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-129">[out] A pointer to the previous status of the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a6b8d-130">戻り値</span><span class="sxs-lookup"><span data-stu-id="a6b8d-130">Return value</span></span>

<span data-ttu-id="a6b8d-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="a6b8d-131">S_OK</span></span> 
  
> <span data-ttu-id="a6b8d-132">メッセージの状態が正常に設定されました。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-132">The message status was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a6b8d-133">解説</span><span class="sxs-lookup"><span data-stu-id="a6b8d-133">Remarks</span></span>

<span data-ttu-id="a6b8d-134">**imapifolder:: setmessagestatus**メソッドは、メッセージの状態を**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティに格納されている値に設定します。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-134">The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a6b8d-135">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="a6b8d-135">Notes to implementers</span></span>

<span data-ttu-id="a6b8d-136">メッセージ状態のビットがどのように設定、クリア、使用されるかは、実装に完全に依存します。ただし、ビット 0 ~ 15 は予約されており、0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-136">How the message status bits are set, cleared, and used depends completely on your implementation, except that bits 0 through 15 are reserved and must be zero.</span></span> 
  
<span data-ttu-id="a6b8d-137">リモートトランスポートプロバイダーのこのメソッドの実装は、ここで説明するセマンティクスに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-137">A remote transport provider's implementation of this method must follow the semantics described here.</span></span> <span data-ttu-id="a6b8d-138">特別な考慮事項はありません。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-138">There are no special considerations.</span></span> <span data-ttu-id="a6b8d-139">クライアントはこのメソッドを使用して、MSGSTATUS_REMOTE_DOWNLOAD および MSGSTATUS_REMOTE_DELETE ビットを設定し、リモートメッセージストアから特定のメッセージをダウンロードまたは削除することを示します。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-139">Clients use this method to set the MSGSTATUS_REMOTE_DOWNLOAD and MSGSTATUS_REMOTE_DELETE bits to indicate that a particular message is to be downloaded or deleted from the remote message store.</span></span> <span data-ttu-id="a6b8d-140">リモートトランスポートプロバイダーは、関連する[imapifolder:: getmessagestatus](imapifolder-getmessagestatus.md)メソッドを実装する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-140">A remote transport provider does not have to implement the related [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) method.</span></span> <span data-ttu-id="a6b8d-141">クライアントは、フォルダーの contents テーブルを調べて、メッセージの状態を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-141">Clients must look in the folder's contents table to determine the status of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a6b8d-142">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a6b8d-142">Notes to callers</span></span>

<span data-ttu-id="a6b8d-143">メッセージの**PR_MSG_STATUS**プロパティを使用して、他のクライアントとのメッセージロックアウト操作をネゴシエートできます。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-143">You can use the **PR_MSG_STATUS** property of a message to negotiate a message lockout operation with other clients.</span></span> <span data-ttu-id="a6b8d-144">ロックアウトビットとしてビットを指定します。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-144">Designate a bit as the lockout bit.</span></span> <span data-ttu-id="a6b8d-145">ロックアウトビットが設定されているかどうかを確認するには、 _lpuloldstatus_パラメーターのメッセージの状態について前の値を調べます。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-145">To determine whether the lockout bit was set, examine the previous value for message status in the  _lpulOldStatus_ parameter.</span></span> <span data-ttu-id="a6b8d-146">_ulnewstatus_パラメーターの他のビットを使用して、ロックアウトビットを妨げることなくメッセージの状態を追跡します。</span><span class="sxs-lookup"><span data-stu-id="a6b8d-146">Use the other bits in the  _ulNewStatus_ parameter to track message status without interfering with the lockout bit.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a6b8d-147">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6b8d-147">See also</span></span>



[<span data-ttu-id="a6b8d-148">IMAPIFolder::GetMessageStatus</span><span class="sxs-lookup"><span data-stu-id="a6b8d-148">IMAPIFolder::GetMessageStatus</span></span>](imapifolder-getmessagestatus.md)
  
[<span data-ttu-id="a6b8d-149">PidTagMessageStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a6b8d-149">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="a6b8d-150">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="a6b8d-150">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)

