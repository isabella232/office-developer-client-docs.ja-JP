---
title: NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFICATION
api_type:
- COM
ms.assetid: 01b6e695-a649-4efd-a893-7586b476467e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280100"
---
# <a name="notification"></a><span data-ttu-id="77445-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="77445-103">NOTIFICATION</span></span>
 
<span data-ttu-id="77445-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77445-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77445-105">発生したイベントおよびイベントの影響を受けたデータに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="77445-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77445-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="77445-106">Header file:</span></span>  <br/> |<span data-ttu-id="77445-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="77445-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulEventType;
  union
  {
    ERROR_NOTIFICATION err;
    NEWMAIL_NOTIFICATION newmail;
    OBJECT_NOTIFICATION obj;
    TABLE_NOTIFICATION tab;
    EXTENDED_NOTIFICATION ext;
    STATUS_OBJECT_NOTIFICATION statobj;
  } info;
} NOTIFICATION, FAR *LPNOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="77445-108">Members</span><span class="sxs-lookup"><span data-stu-id="77445-108">Members</span></span>

<span data-ttu-id="77445-109">**uleventtype**</span><span class="sxs-lookup"><span data-stu-id="77445-109">**ulEventType**</span></span>
  
> <span data-ttu-id="77445-110">発生した通知イベントの種類。</span><span class="sxs-lookup"><span data-stu-id="77445-110">Type of notification event that occurred.</span></span> <span data-ttu-id="77445-111">**uleventtype**メンバーの値は、 **info**ユニオンに含まれている構造に対応しています。</span><span class="sxs-lookup"><span data-stu-id="77445-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="77445-112">**uleventtype**メンバーは、次のいずれかの値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="77445-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="77445-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="77445-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="77445-114">グローバルなエラーが発生しました。セッションが進行中にシャットダウンされた場合などです。</span><span class="sxs-lookup"><span data-stu-id="77445-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="77445-115">**info**メンバーには、 [ERROR_NOTIFICATION](error_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="77445-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="77445-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="77445-117">特定のサービスプロバイダーによって定義された内部イベントが発生しました。</span><span class="sxs-lookup"><span data-stu-id="77445-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="77445-118">**info**メンバーには、 [EXTENDED_NOTIFICATION](extended_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="77445-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="77445-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="77445-120">メッセージは、メッセージクラスの適切な受信フォルダーに配信され、処理を待機しています。</span><span class="sxs-lookup"><span data-stu-id="77445-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="77445-121">**info**メンバーには、 [NEWMAIL_NOTIFICATION](newmail_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="77445-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="77445-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="77445-123">MAPI オブジェクトがコピーされました。</span><span class="sxs-lookup"><span data-stu-id="77445-123">A MAPI object has been copied.</span></span> <span data-ttu-id="77445-124">**info**メンバーには、 [OBJECT_NOTIFICATION](object_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="77445-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="77445-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="77445-126">MAPI オブジェクトが作成されました。</span><span class="sxs-lookup"><span data-stu-id="77445-126">A MAPI object has been created.</span></span> <span data-ttu-id="77445-127">**info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="77445-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="77445-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="77445-129">MAPI オブジェクトが削除されました。</span><span class="sxs-lookup"><span data-stu-id="77445-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="77445-130">**info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="77445-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="77445-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="77445-132">MAPI オブジェクトが変更されました。</span><span class="sxs-lookup"><span data-stu-id="77445-132">A MAPI object has changed.</span></span> <span data-ttu-id="77445-133">**info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="77445-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="77445-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="77445-135">メッセージストアまたはアドレス帳オブジェクトが移動されました。</span><span class="sxs-lookup"><span data-stu-id="77445-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="77445-136">**info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="77445-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="77445-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="77445-138">検索操作が終了し、結果を使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="77445-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="77445-139">**info**メンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="77445-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="77445-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="77445-141">テーブル内の情報が変更されました。</span><span class="sxs-lookup"><span data-stu-id="77445-141">Information in a table has changed.</span></span> <span data-ttu-id="77445-142">**info**メンバーには、 [TABLE_NOTIFICATION](table_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="77445-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="77445-143">**info**</span><span class="sxs-lookup"><span data-stu-id="77445-143">**info**</span></span>
  
> <span data-ttu-id="77445-144">特定の種類のイベントの影響を受けるデータを記述する通知構造の和集合。</span><span class="sxs-lookup"><span data-stu-id="77445-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="77445-145">**info**メンバーに含まれる構造は、 **uleventtype**メンバーの値に依存します。</span><span class="sxs-lookup"><span data-stu-id="77445-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="77445-146">解説</span><span class="sxs-lookup"><span data-stu-id="77445-146">Remarks</span></span>

<span data-ttu-id="77445-147">登録されたアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドへのすべての呼び出しで、1つ以上の**通知**構造が入力パラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="77445-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="77445-148">**通知**構造には、発生した特定のイベントに関する情報が含まれ、影響を受けるオブジェクトについて説明します。</span><span class="sxs-lookup"><span data-stu-id="77445-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="77445-149">通知を受け取るクライアントまたはサービスプロバイダーは、構造体を使用してイベントを処理する前に、 **uleventtype**メンバーに示されているように、イベントの種類を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="77445-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="77445-150">たとえば、次に示すコードサンプルでは、新しいメッセージの到着をチェックし、この種のイベントを検出すると、メッセージのメッセージクラスを出力します。</span><span class="sxs-lookup"><span data-stu-id="77445-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="77445-151">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="77445-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="77445-152">**トピック**</span><span class="sxs-lookup"><span data-stu-id="77445-152">**Topic**</span></span>|<span data-ttu-id="77445-153">**説明**</span><span class="sxs-lookup"><span data-stu-id="77445-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="77445-154">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="77445-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="77445-155">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="77445-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="77445-156">通知の処理</span><span class="sxs-lookup"><span data-stu-id="77445-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="77445-157">クライアントが通知を処理する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="77445-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="77445-158">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="77445-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="77445-159">サービスプロバイダーが[imapisupport](imapisupportiunknown.md)メソッドを使用して通知を生成する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="77445-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="77445-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="77445-160">See also</span></span>


- [<span data-ttu-id="77445-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="77445-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="77445-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="77445-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="77445-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="77445-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="77445-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="77445-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="77445-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="77445-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="77445-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="77445-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="77445-167">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="77445-167">MAPI Structures</span></span>](mapi-structures.md)

