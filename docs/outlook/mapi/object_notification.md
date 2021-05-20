---
title: OBJECT_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OBJECT_NOTIFICATION
api_type:
- COM
ms.assetid: de3a2297-e0cc-427b-a978-52bade4d9bce
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430169"
---
# <a name="object_notification"></a><span data-ttu-id="5084a-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5084a-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="5084a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5084a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5084a-105">コピーや変更など、変更を受けたオブジェクトに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="5084a-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5084a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5084a-106">Header file:</span></span>  <br/> |<span data-ttu-id="5084a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5084a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _OBJECT_NOTIFICATION
{
  ULONG cbEntryID;
  LPENTRYID lpEntryID;
  ULONG ulObjType;
  ULONG cbParentID;
  LPENTRYID lpParentID;
  ULONG cbOldID;
  LPENTRYID lpOldID;
  ULONG cbOldParentID;
  LPENTRYID lpOldParentID;
  LPSPropTagArray lpPropTagArray;
} OBJECT_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="5084a-108">Members</span><span class="sxs-lookup"><span data-stu-id="5084a-108">Members</span></span>

 <span data-ttu-id="5084a-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="5084a-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="5084a-110">**lpEntryID** メンバーが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="5084a-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="5084a-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="5084a-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="5084a-112">影響を受けるオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5084a-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="5084a-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="5084a-113">**ulObjType**</span></span>
  
> <span data-ttu-id="5084a-114">影響を受けるオブジェクトの種類。</span><span class="sxs-lookup"><span data-stu-id="5084a-114">Type of object affected.</span></span> <span data-ttu-id="5084a-115">使用できる型は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5084a-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="5084a-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="5084a-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="5084a-117">メッセージ ストア。</span><span class="sxs-lookup"><span data-stu-id="5084a-117">Message store.</span></span> 
    
<span data-ttu-id="5084a-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="5084a-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="5084a-119">アドレス帳。</span><span class="sxs-lookup"><span data-stu-id="5084a-119">Address book.</span></span> 
    
<span data-ttu-id="5084a-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="5084a-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="5084a-121">フォルダー。</span><span class="sxs-lookup"><span data-stu-id="5084a-121">Folder.</span></span>
    
<span data-ttu-id="5084a-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="5084a-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="5084a-123">アドレス帳コンテナー。</span><span class="sxs-lookup"><span data-stu-id="5084a-123">Address book container.</span></span>
    
<span data-ttu-id="5084a-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="5084a-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="5084a-125">メッセージ。</span><span class="sxs-lookup"><span data-stu-id="5084a-125">Message.</span></span>
    
<span data-ttu-id="5084a-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="5084a-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="5084a-127">メッセージング ユーザー。</span><span class="sxs-lookup"><span data-stu-id="5084a-127">Messaging user.</span></span>
    
<span data-ttu-id="5084a-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="5084a-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="5084a-129">添付ファイル。</span><span class="sxs-lookup"><span data-stu-id="5084a-129">Attachment.</span></span>
    
<span data-ttu-id="5084a-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="5084a-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="5084a-131">配布リスト。</span><span class="sxs-lookup"><span data-stu-id="5084a-131">Distribution list.</span></span>
    
<span data-ttu-id="5084a-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="5084a-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="5084a-133">[プロファイル] セクション。</span><span class="sxs-lookup"><span data-stu-id="5084a-133">Profile section.</span></span>
    
<span data-ttu-id="5084a-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="5084a-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="5084a-135">Status オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5084a-135">Status object.</span></span>
    
<span data-ttu-id="5084a-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="5084a-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="5084a-137">Session オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5084a-137">Session object.</span></span>
    
 <span data-ttu-id="5084a-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="5084a-138">**cbParentID**</span></span>
  
> <span data-ttu-id="5084a-139">**lpParentID** メンバーが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="5084a-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="5084a-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="5084a-140">**lpParentID**</span></span>
  
> <span data-ttu-id="5084a-141">影響を受けるオブジェクトの親のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5084a-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="5084a-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="5084a-142">**cbOldID**</span></span>
  
> <span data-ttu-id="5084a-143">**lpOldID** メンバーが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="5084a-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="5084a-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="5084a-144">**lpOldID**</span></span>
  
> <span data-ttu-id="5084a-145">元のオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5084a-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="5084a-146">イベントで元のオブジェクトが必要ない場合は、このポインターを NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="5084a-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="5084a-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="5084a-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="5084a-148">**lpOldParentID** メンバーが指すエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="5084a-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="5084a-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="5084a-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="5084a-150">元のオブジェクトの親のエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5084a-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="5084a-151">イベントで元のオブジェクトが必要ない場合は、このポインターを NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="5084a-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="5084a-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="5084a-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="5084a-153">イベントの影響 [を受けるプロパティを](sproptagarray.md) 識別するプロパティ タグを含む SPropTagArray 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5084a-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5084a-154">注釈</span><span class="sxs-lookup"><span data-stu-id="5084a-154">Remarks</span></span>

<span data-ttu-id="5084a-155">この **OBJECT_NOTIFICATION** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体 **のメンバー** の [1](notification.md) つです。</span><span class="sxs-lookup"><span data-stu-id="5084a-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="5084a-156">**NOTIFICATION** **構造体の info** メンバーに OBJECT_NOTIFICATION構造体が含まれている場合 **、NOTIFICATION** 構造体の **ulEventType** メンバーは、次のいずれかの種類のイベントに設定されます。</span><span class="sxs-lookup"><span data-stu-id="5084a-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="5084a-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="5084a-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="5084a-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="5084a-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="5084a-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="5084a-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="5084a-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="5084a-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="5084a-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="5084a-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="5084a-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="5084a-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="5084a-163">fnevSearchComplete イベントの種類で表される検索完了イベントは、1 つの検索フォルダーのドメインの最初の検索が完了したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="5084a-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="5084a-164">元のオブジェクトに関する情報を含む次のメンバーは、移動イベントとコピー イベントでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="5084a-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="5084a-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="5084a-165">**cbOldID**</span></span>
    
- <span data-ttu-id="5084a-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="5084a-166">**lpOldID**</span></span>
    
- <span data-ttu-id="5084a-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="5084a-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="5084a-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="5084a-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="5084a-169">これらのメンバーは、他の種類のイベントには適用されません。</span><span class="sxs-lookup"><span data-stu-id="5084a-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="5084a-170">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5084a-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="5084a-171">**トピック**</span><span class="sxs-lookup"><span data-stu-id="5084a-171">**Topic**</span></span>|<span data-ttu-id="5084a-172">**説明**</span><span class="sxs-lookup"><span data-stu-id="5084a-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5084a-173">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="5084a-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="5084a-174">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="5084a-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="5084a-175">通知の処理</span><span class="sxs-lookup"><span data-stu-id="5084a-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="5084a-176">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5084a-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="5084a-177">サポート イベント通知</span><span class="sxs-lookup"><span data-stu-id="5084a-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="5084a-178">サービス プロバイダーが [IMAPISupport](imapisupportiunknown.md) メソッドを使用して通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5084a-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5084a-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="5084a-179">See also</span></span>



[<span data-ttu-id="5084a-180">�ʒm</span><span class="sxs-lookup"><span data-stu-id="5084a-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="5084a-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="5084a-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="5084a-182">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="5084a-182">MAPI Structures</span></span>](mapi-structures.md)

