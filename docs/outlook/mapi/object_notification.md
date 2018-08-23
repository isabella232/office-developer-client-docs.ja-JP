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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1593152786a3345827089e5f6702454896944b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801676"
---
# <a name="objectnotification"></a><span data-ttu-id="ecd5a-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="ecd5a-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="ecd5a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecd5a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecd5a-105">変更が行われて、次のようにしてコピーまたは変更されたオブジェクトに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecd5a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ecd5a-106">Header file:</span></span>  <br/> |<span data-ttu-id="ecd5a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecd5a-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="ecd5a-108">Members</span><span class="sxs-lookup"><span data-stu-id="ecd5a-108">Members</span></span>

 <span data-ttu-id="ecd5a-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="ecd5a-110">**LpEntryID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="ecd5a-111">**lpEntryID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="ecd5a-112">影響を受けるオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="ecd5a-113">**ulObjType**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-113">**ulObjType**</span></span>
  
> <span data-ttu-id="ecd5a-114">影響を受けるオブジェクトの種類です。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-114">Type of object affected.</span></span> <span data-ttu-id="ecd5a-115">使用可能な型は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="ecd5a-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="ecd5a-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="ecd5a-117">メッセージ ・ ストアです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-117">Message store.</span></span> 
    
<span data-ttu-id="ecd5a-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="ecd5a-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="ecd5a-119">アドレス帳です。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-119">Address book.</span></span> 
    
<span data-ttu-id="ecd5a-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="ecd5a-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="ecd5a-121">フォルダーです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-121">Folder.</span></span>
    
<span data-ttu-id="ecd5a-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="ecd5a-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="ecd5a-123">アドレス帳コンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-123">Address book container.</span></span>
    
<span data-ttu-id="ecd5a-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="ecd5a-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="ecd5a-125">メッセージ。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-125">Message.</span></span>
    
<span data-ttu-id="ecd5a-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="ecd5a-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="ecd5a-127">メッセージングのユーザーです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-127">Messaging user.</span></span>
    
<span data-ttu-id="ecd5a-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="ecd5a-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="ecd5a-129">添付ファイルです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-129">Attachment.</span></span>
    
<span data-ttu-id="ecd5a-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="ecd5a-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="ecd5a-131">配布リストです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-131">Distribution list.</span></span>
    
<span data-ttu-id="ecd5a-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="ecd5a-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="ecd5a-133">プロファイル セクションです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-133">Profile section.</span></span>
    
<span data-ttu-id="ecd5a-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="ecd5a-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="ecd5a-135">状態オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-135">Status object.</span></span>
    
<span data-ttu-id="ecd5a-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="ecd5a-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="ecd5a-137">セッション オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-137">Session object.</span></span>
    
 <span data-ttu-id="ecd5a-138">**cbParentID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-138">**cbParentID**</span></span>
  
> <span data-ttu-id="ecd5a-139">**LpParentID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="ecd5a-140">**lpParentID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-140">**lpParentID**</span></span>
  
> <span data-ttu-id="ecd5a-141">影響を受けるオブジェクトの親オブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="ecd5a-142">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-142">**cbOldID**</span></span>
  
> <span data-ttu-id="ecd5a-143">**LpOldID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="ecd5a-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-144">**lpOldID**</span></span>
  
> <span data-ttu-id="ecd5a-145">元のオブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="ecd5a-146">イベントが元のオブジェクトを必要としない場合は、このポインターを NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="ecd5a-147">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="ecd5a-148">**LpOldParentID**メンバーが指すエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="ecd5a-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="ecd5a-150">元のオブジェクトの親オブジェクトのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="ecd5a-151">イベントが元のオブジェクトを必要としない場合は、このポインターを NULL にできます。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="ecd5a-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="ecd5a-153">イベントによって影響を受けるプロパティを識別するプロパティ タグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ecd5a-154">注釈</span><span class="sxs-lookup"><span data-stu-id="ecd5a-154">Remarks</span></span>

<span data-ttu-id="ecd5a-155">**OBJECT_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="ecd5a-156">**通知**の構造体のメンバー**情報**には、 **OBJECT_NOTIFICATION**構造体が含まれている、**通知**の構造体の**ulEventType**メンバーは、次の種類のイベントのいずれかに設定されます。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="ecd5a-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="ecd5a-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="ecd5a-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="ecd5a-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="ecd5a-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="ecd5a-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="ecd5a-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="ecd5a-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="ecd5a-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="ecd5a-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="ecd5a-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="ecd5a-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="ecd5a-163">FnevSearchComplete イベントの種類によって表される、検索の完了イベントは、ドメインの 1 つの検索フォルダーを最初に検索が完了したことを示します。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="ecd5a-164">元のオブジェクトに関する情報が含まれている次のメンバーは、移動およびコピーのイベントでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="ecd5a-165">**cbOldID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-165">**cbOldID**</span></span>
    
- <span data-ttu-id="ecd5a-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-166">**lpOldID**</span></span>
    
- <span data-ttu-id="ecd5a-167">**cbOldParentID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="ecd5a-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="ecd5a-169">これらのメンバーは、他の種類のイベントには適用されません。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="ecd5a-170">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="ecd5a-171">**トピック**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-171">**Topic**</span></span>|<span data-ttu-id="ecd5a-172">**説明**</span><span class="sxs-lookup"><span data-stu-id="ecd5a-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ecd5a-173">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="ecd5a-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="ecd5a-174">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="ecd5a-175">通知の処理</span><span class="sxs-lookup"><span data-stu-id="ecd5a-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="ecd5a-176">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="ecd5a-177">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="ecd5a-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="ecd5a-178">サービス プロバイダーが、 [IMAPISupport](imapisupportiunknown.md)メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ecd5a-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ecd5a-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecd5a-179">See also</span></span>



[<span data-ttu-id="ecd5a-180">�ʒm</span><span class="sxs-lookup"><span data-stu-id="ecd5a-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="ecd5a-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ecd5a-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="ecd5a-182">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="ecd5a-182">MAPI Structures</span></span>](mapi-structures.md)

