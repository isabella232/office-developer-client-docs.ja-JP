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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a3235c2305d61318f482943167e5f307e5da0d70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432878"
---
# <a name="notification"></a><span data-ttu-id="7a614-103">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a614-103">NOTIFICATION</span></span>
 
<span data-ttu-id="7a614-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a614-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a614-105">発生したイベントと、イベントの影響を受けたデータに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="7a614-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a614-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7a614-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a614-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a614-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="7a614-108">Members</span><span class="sxs-lookup"><span data-stu-id="7a614-108">Members</span></span>

<span data-ttu-id="7a614-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="7a614-109">**ulEventType**</span></span>
  
> <span data-ttu-id="7a614-110">発生した通知イベントの種類。</span><span class="sxs-lookup"><span data-stu-id="7a614-110">Type of notification event that occurred.</span></span> <span data-ttu-id="7a614-111">**ulEventType メンバーの値** は、情報ユニオンに含まれる構造に **対応** します。</span><span class="sxs-lookup"><span data-stu-id="7a614-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="7a614-112">**ulEventType メンバー** は、次のいずれかの値に設定できます。</span><span class="sxs-lookup"><span data-stu-id="7a614-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="7a614-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="7a614-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="7a614-114">進行中のセッションのシャットダウンなど、グローバル エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="7a614-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="7a614-115">info **メンバー** には、新しい構造 [ERROR_NOTIFICATION](error_notification.md) 含まれる。</span><span class="sxs-lookup"><span data-stu-id="7a614-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="7a614-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="7a614-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="7a614-117">特定のサービス プロバイダーによって定義された内部イベントが発生しました。</span><span class="sxs-lookup"><span data-stu-id="7a614-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="7a614-118">info **メンバー** には、新 [しいEXTENDED_NOTIFICATION](extended_notification.md) があります。</span><span class="sxs-lookup"><span data-stu-id="7a614-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="7a614-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="7a614-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="7a614-120">メッセージがメッセージ クラスの適切な受信フォルダーに配信され、処理を待機しています。</span><span class="sxs-lookup"><span data-stu-id="7a614-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="7a614-121">info **メンバー** には、特定の構造 [NEWMAIL_NOTIFICATION](newmail_notification.md) があります。</span><span class="sxs-lookup"><span data-stu-id="7a614-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="7a614-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="7a614-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="7a614-123">MAPI オブジェクトがコピーされました。</span><span class="sxs-lookup"><span data-stu-id="7a614-123">A MAPI object has been copied.</span></span> <span data-ttu-id="7a614-124">info **メンバー** には、次 [のOBJECT_NOTIFICATIONがあります](object_notification.md) 。</span><span class="sxs-lookup"><span data-stu-id="7a614-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="7a614-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="7a614-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="7a614-126">MAPI オブジェクトが作成されました。</span><span class="sxs-lookup"><span data-stu-id="7a614-126">A MAPI object has been created.</span></span> <span data-ttu-id="7a614-127">info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。</span><span class="sxs-lookup"><span data-stu-id="7a614-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="7a614-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="7a614-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="7a614-129">MAPI オブジェクトが削除されました。</span><span class="sxs-lookup"><span data-stu-id="7a614-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="7a614-130">info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。</span><span class="sxs-lookup"><span data-stu-id="7a614-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="7a614-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="7a614-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="7a614-132">MAPI オブジェクトが変更されました。</span><span class="sxs-lookup"><span data-stu-id="7a614-132">A MAPI object has changed.</span></span> <span data-ttu-id="7a614-133">info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。</span><span class="sxs-lookup"><span data-stu-id="7a614-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="7a614-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="7a614-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="7a614-135">メッセージ ストアまたはアドレス帳オブジェクトが移動されました。</span><span class="sxs-lookup"><span data-stu-id="7a614-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="7a614-136">info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。</span><span class="sxs-lookup"><span data-stu-id="7a614-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="7a614-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="7a614-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="7a614-138">検索操作が完了し、結果を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7a614-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="7a614-139">info **メンバー** には、次 **のOBJECT_NOTIFICATIONがあります** 。</span><span class="sxs-lookup"><span data-stu-id="7a614-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="7a614-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="7a614-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="7a614-141">テーブル内の情報が変更されました。</span><span class="sxs-lookup"><span data-stu-id="7a614-141">Information in a table has changed.</span></span> <span data-ttu-id="7a614-142">info **メンバー** には、新しい構造 [TABLE_NOTIFICATION](table_notification.md) があります。</span><span class="sxs-lookup"><span data-stu-id="7a614-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="7a614-143">**info**</span><span class="sxs-lookup"><span data-stu-id="7a614-143">**info**</span></span>
  
> <span data-ttu-id="7a614-144">特定の種類のイベントの影響を受けるデータを記述する通知構造のユニオン。</span><span class="sxs-lookup"><span data-stu-id="7a614-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="7a614-145">info メンバーに含まれる構造は **、ulEventType メンバーの値によって異** なります。 </span><span class="sxs-lookup"><span data-stu-id="7a614-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7a614-146">注釈</span><span class="sxs-lookup"><span data-stu-id="7a614-146">Remarks</span></span>

<span data-ttu-id="7a614-147">1 つ以上 **の NOTIFICATION** 構造体は、登録されたアアドバイス シンクの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドへのすべての呼び出しで入力パラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="7a614-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="7a614-148">**NOTIFICATION 構造体** には、発生した特定のイベントに関する情報と、影響を受けるオブジェクトの説明が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7a614-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="7a614-149">通知を受け取るクライアントまたはサービス プロバイダーが構造を使用してイベントを処理する前に **、ulEventType** メンバーに示されているイベントの種類を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a614-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="7a614-150">たとえば、次に示すコード サンプルは、新しいメッセージの到着を確認し、この種のイベントを検出すると、メッセージのメッセージ クラスを出力します。</span><span class="sxs-lookup"><span data-stu-id="7a614-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="7a614-151">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7a614-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="7a614-152">**トピック**</span><span class="sxs-lookup"><span data-stu-id="7a614-152">**Topic**</span></span>|<span data-ttu-id="7a614-153">**説明**</span><span class="sxs-lookup"><span data-stu-id="7a614-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7a614-154">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="7a614-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="7a614-155">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="7a614-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="7a614-156">通知の処理</span><span class="sxs-lookup"><span data-stu-id="7a614-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="7a614-157">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a614-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="7a614-158">サポート イベント通知</span><span class="sxs-lookup"><span data-stu-id="7a614-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="7a614-159">サービス プロバイダーが [IMAPISupport](imapisupportiunknown.md) メソッドを使用して通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7a614-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a614-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a614-160">See also</span></span>


- [<span data-ttu-id="7a614-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a614-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="7a614-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a614-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="7a614-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a614-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="7a614-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a614-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="7a614-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a614-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="7a614-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="7a614-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="7a614-167">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="7a614-167">MAPI Structures</span></span>](mapi-structures.md)

