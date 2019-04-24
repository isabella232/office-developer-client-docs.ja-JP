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
ms.openlocfilehash: c637b3b03a22f208123397f7277cf8968f2509a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279887"
---
# <a name="objectnotification"></a><span data-ttu-id="cc11f-103">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="cc11f-103">OBJECT_NOTIFICATION</span></span>

  
  
<span data-ttu-id="cc11f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc11f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc11f-105">コピー、変更など、変更されたオブジェクトに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="cc11f-105">Contains information about an object that has undergone a change, such as being copied or modified.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc11f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cc11f-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc11f-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cc11f-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="cc11f-108">Members</span><span class="sxs-lookup"><span data-stu-id="cc11f-108">Members</span></span>

 <span data-ttu-id="cc11f-109">**cbEntryID**</span><span class="sxs-lookup"><span data-stu-id="cc11f-109">**cbEntryID**</span></span>
  
> <span data-ttu-id="cc11f-110">**lな tryid**メンバーによって指摘されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="cc11f-110">Count of bytes in the entry identifier pointed to by the **lpEntryID** member.</span></span> 
    
 <span data-ttu-id="cc11f-111">**lて tryid**</span><span class="sxs-lookup"><span data-stu-id="cc11f-111">**lpEntryID**</span></span>
  
> <span data-ttu-id="cc11f-112">影響を受けるオブジェクトのエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc11f-112">Pointer to the entry identifier of the affected object.</span></span>
    
 <span data-ttu-id="cc11f-113">**ulobjtype**</span><span class="sxs-lookup"><span data-stu-id="cc11f-113">**ulObjType**</span></span>
  
> <span data-ttu-id="cc11f-114">影響を受けるオブジェクトの種類。</span><span class="sxs-lookup"><span data-stu-id="cc11f-114">Type of object affected.</span></span> <span data-ttu-id="cc11f-115">可能な種類は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cc11f-115">Possible types are as follows:</span></span>
    
<span data-ttu-id="cc11f-116">MAPI_STORE</span><span class="sxs-lookup"><span data-stu-id="cc11f-116">MAPI_STORE</span></span> 
  
> <span data-ttu-id="cc11f-117">メッセージストア。</span><span class="sxs-lookup"><span data-stu-id="cc11f-117">Message store.</span></span> 
    
<span data-ttu-id="cc11f-118">MAPI_ADDRBOOK</span><span class="sxs-lookup"><span data-stu-id="cc11f-118">MAPI_ADDRBOOK</span></span> 
  
> <span data-ttu-id="cc11f-119">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="cc11f-119">Address book.</span></span> 
    
<span data-ttu-id="cc11f-120">MAPI_FOLDER</span><span class="sxs-lookup"><span data-stu-id="cc11f-120">MAPI_FOLDER</span></span> 
  
> <span data-ttu-id="cc11f-121">].</span><span class="sxs-lookup"><span data-stu-id="cc11f-121">Folder.</span></span>
    
<span data-ttu-id="cc11f-122">MAPI_ABCONT</span><span class="sxs-lookup"><span data-stu-id="cc11f-122">MAPI_ABCONT</span></span> 
  
> <span data-ttu-id="cc11f-123">アドレス帳のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="cc11f-123">Address book container.</span></span>
    
<span data-ttu-id="cc11f-124">MAPI_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="cc11f-124">MAPI_MESSAGE</span></span> 
  
> <span data-ttu-id="cc11f-125">メッセージ。</span><span class="sxs-lookup"><span data-stu-id="cc11f-125">Message.</span></span>
    
<span data-ttu-id="cc11f-126">MAPI_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="cc11f-126">MAPI_MAILUSER</span></span> 
  
> <span data-ttu-id="cc11f-127">メッセージングユーザー。</span><span class="sxs-lookup"><span data-stu-id="cc11f-127">Messaging user.</span></span>
    
<span data-ttu-id="cc11f-128">MAPI_ATTACH</span><span class="sxs-lookup"><span data-stu-id="cc11f-128">MAPI_ATTACH</span></span> 
  
> <span data-ttu-id="cc11f-129">資料.</span><span class="sxs-lookup"><span data-stu-id="cc11f-129">Attachment.</span></span>
    
<span data-ttu-id="cc11f-130">MAPI_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="cc11f-130">MAPI_DISTLIST</span></span> 
  
> <span data-ttu-id="cc11f-131">配布リスト</span><span class="sxs-lookup"><span data-stu-id="cc11f-131">Distribution list.</span></span>
    
<span data-ttu-id="cc11f-132">MAPI_PROFSECT</span><span class="sxs-lookup"><span data-stu-id="cc11f-132">MAPI_PROFSECT</span></span> 
  
> <span data-ttu-id="cc11f-133">プロファイルセクション。</span><span class="sxs-lookup"><span data-stu-id="cc11f-133">Profile section.</span></span>
    
<span data-ttu-id="cc11f-134">MAPI_STATUS</span><span class="sxs-lookup"><span data-stu-id="cc11f-134">MAPI_STATUS</span></span> 
  
> <span data-ttu-id="cc11f-135">Status オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="cc11f-135">Status object.</span></span>
    
<span data-ttu-id="cc11f-136">MAPI_SESSION</span><span class="sxs-lookup"><span data-stu-id="cc11f-136">MAPI_SESSION</span></span> 
  
> <span data-ttu-id="cc11f-137">Session オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="cc11f-137">Session object.</span></span>
    
 <span data-ttu-id="cc11f-138">**cbparentid**</span><span class="sxs-lookup"><span data-stu-id="cc11f-138">**cbParentID**</span></span>
  
> <span data-ttu-id="cc11f-139">**lpparentid**メンバーによって指摘されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="cc11f-139">Count of bytes in the entry identifier pointed to by the **lpParentID** member.</span></span> 
    
 <span data-ttu-id="cc11f-140">**lpparentid**</span><span class="sxs-lookup"><span data-stu-id="cc11f-140">**lpParentID**</span></span>
  
> <span data-ttu-id="cc11f-141">影響を受けるオブジェクトの親のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc11f-141">Pointer to the entry identifier of the parent of the affected object.</span></span>
    
 <span data-ttu-id="cc11f-142">**cbold did**</span><span class="sxs-lookup"><span data-stu-id="cc11f-142">**cbOldID**</span></span>
  
> <span data-ttu-id="cc11f-143">**lpOldID**メンバーによって示されるエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="cc11f-143">Count of bytes in the entry identifier pointed to by the **lpOldID** member.</span></span> 
    
 <span data-ttu-id="cc11f-144">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="cc11f-144">**lpOldID**</span></span>
  
> <span data-ttu-id="cc11f-145">元のオブジェクトのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc11f-145">Pointer to the entry identifier of the original object.</span></span> <span data-ttu-id="cc11f-146">イベントに元のオブジェクトが必要ない場合は、このポインターを NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc11f-146">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="cc11f-147">**cbold parentid**</span><span class="sxs-lookup"><span data-stu-id="cc11f-147">**cbOldParentID**</span></span>
  
> <span data-ttu-id="cc11f-148">**lpOldParentID**メンバーによって示されるエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="cc11f-148">Count of bytes in the entry identifier pointed to by the **lpOldParentID** member.</span></span> 
    
 <span data-ttu-id="cc11f-149">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="cc11f-149">**lpOldParentID**</span></span>
  
> <span data-ttu-id="cc11f-150">元のオブジェクトの親のエントリ id へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc11f-150">Pointer to the entry identifier of the parent of the original object.</span></span> <span data-ttu-id="cc11f-151">イベントに元のオブジェクトが必要ない場合は、このポインターを NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="cc11f-151">This pointer can be NULL if the event does not require an original object.</span></span>
    
 <span data-ttu-id="cc11f-152">**lpPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="cc11f-152">**lpPropTagArray**</span></span>
  
> <span data-ttu-id="cc11f-153">イベントの影響を受けるプロパティを識別するプロパティタグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc11f-153">Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the property tags identifying properties affected by the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cc11f-154">解説</span><span class="sxs-lookup"><span data-stu-id="cc11f-154">Remarks</span></span>

<span data-ttu-id="cc11f-155">**OBJECT_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="cc11f-155">The **OBJECT_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="cc11f-156">**通知**構造の**info**メンバーに**OBJECT_NOTIFICATION**構造体が含まれている場合、**通知**構造の**uleventtype**メンバーは、次のいずれかの種類のイベントに設定されます。</span><span class="sxs-lookup"><span data-stu-id="cc11f-156">When the **info** member of a **NOTIFICATION** structure contains an **OBJECT_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to one of the following types of events:</span></span> 
  
- <span data-ttu-id="cc11f-157">fnevObjectCreated</span><span class="sxs-lookup"><span data-stu-id="cc11f-157">fnevObjectCreated</span></span>
    
- <span data-ttu-id="cc11f-158">fnevObjectModified</span><span class="sxs-lookup"><span data-stu-id="cc11f-158">fnevObjectModified</span></span>
    
- <span data-ttu-id="cc11f-159">fnevObjectDeleted</span><span class="sxs-lookup"><span data-stu-id="cc11f-159">fnevObjectDeleted</span></span>
    
- <span data-ttu-id="cc11f-160">fnevObjectMoved</span><span class="sxs-lookup"><span data-stu-id="cc11f-160">fnevObjectMoved</span></span>
    
- <span data-ttu-id="cc11f-161">fnevObjectCopied</span><span class="sxs-lookup"><span data-stu-id="cc11f-161">fnevObjectCopied</span></span>
    
- <span data-ttu-id="cc11f-162">fnevSearchComplete</span><span class="sxs-lookup"><span data-stu-id="cc11f-162">fnevSearchComplete</span></span>
    
<span data-ttu-id="cc11f-163">fnevSearchComplete イベントの種類で表される検索の完了イベントは、1つの検索フォルダーのドメインの最初の検索が完了したことを示します。</span><span class="sxs-lookup"><span data-stu-id="cc11f-163">The search complete event, represented by the fnevSearchComplete event type, indicates that the initial search of the domain for one search folder has completed.</span></span>
  
<span data-ttu-id="cc11f-164">元のオブジェクトに関する情報を格納している次のメンバーは、移動イベントとコピーイベントでのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc11f-164">The following members that contain information about the original object are used only in move and copy events.</span></span> 
  
- <span data-ttu-id="cc11f-165">**cbold did**</span><span class="sxs-lookup"><span data-stu-id="cc11f-165">**cbOldID**</span></span>
    
- <span data-ttu-id="cc11f-166">**lpOldID**</span><span class="sxs-lookup"><span data-stu-id="cc11f-166">**lpOldID**</span></span>
    
- <span data-ttu-id="cc11f-167">**cbold parentid**</span><span class="sxs-lookup"><span data-stu-id="cc11f-167">**cbOldParentID**</span></span>
    
- <span data-ttu-id="cc11f-168">**lpOldParentID**</span><span class="sxs-lookup"><span data-stu-id="cc11f-168">**lpOldParentID**</span></span>
    
<span data-ttu-id="cc11f-169">これらのメンバーは、他の種類のイベントには適用されません。</span><span class="sxs-lookup"><span data-stu-id="cc11f-169">These members do not apply to the other types of events.</span></span>
  
<span data-ttu-id="cc11f-170">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc11f-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="cc11f-171">**トピック**</span><span class="sxs-lookup"><span data-stu-id="cc11f-171">**Topic**</span></span>|<span data-ttu-id="cc11f-172">**説明**</span><span class="sxs-lookup"><span data-stu-id="cc11f-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cc11f-173">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="cc11f-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="cc11f-174">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="cc11f-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="cc11f-175">通知の処理</span><span class="sxs-lookup"><span data-stu-id="cc11f-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="cc11f-176">クライアントが通知を処理する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="cc11f-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="cc11f-177">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="cc11f-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="cc11f-178">サービスプロバイダーが[imapisupport](imapisupportiunknown.md)メソッドを使用して通知を生成する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="cc11f-178">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cc11f-179">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc11f-179">See also</span></span>



[<span data-ttu-id="cc11f-180">�ʒm</span><span class="sxs-lookup"><span data-stu-id="cc11f-180">NOTIFICATION</span></span>](notification.md)
  
[<span data-ttu-id="cc11f-181">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="cc11f-181">SPropTagArray</span></span>](sproptagarray.md)


[<span data-ttu-id="cc11f-182">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="cc11f-182">MAPI Structures</span></span>](mapi-structures.md)

