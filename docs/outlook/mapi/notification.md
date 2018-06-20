---
title: 通知
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7a8d25dc7cac4226f38baab593b254108210549e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801683"
---
# <a name="notification"></a><span data-ttu-id="71c15-103">通知</span><span class="sxs-lookup"><span data-stu-id="71c15-103">NOTIFICATION</span></span>
 
<span data-ttu-id="71c15-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="71c15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="71c15-105">イベントが発生したことと、イベントによって影響のあるデータに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-105">Contains information about an event that has occurred and the data that has been affected by the event.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71c15-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="71c15-106">Header file:</span></span>  <br/> |<span data-ttu-id="71c15-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="71c15-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="71c15-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="71c15-108">Members</span></span>

<span data-ttu-id="71c15-109">**ulEventType**</span><span class="sxs-lookup"><span data-stu-id="71c15-109">**ulEventType**</span></span>
  
> <span data-ttu-id="71c15-110">発生した通知イベントの種類です。</span><span class="sxs-lookup"><span data-stu-id="71c15-110">Type of notification event that occurred.</span></span> <span data-ttu-id="71c15-111">**UlEventType**メンバーの値は、**情報**の共用体に含まれる構造体に対応します。</span><span class="sxs-lookup"><span data-stu-id="71c15-111">The value of the **ulEventType** member corresponds to the structure that is included in the **info** union.</span></span> <span data-ttu-id="71c15-112">**UlEventType**メンバーは、次の値のいずれかに設定できます。</span><span class="sxs-lookup"><span data-stu-id="71c15-112">The **ulEventType** member can be set to one of the following values:</span></span> 
    
 <span data-ttu-id="71c15-113">_fnevCriticalError_</span><span class="sxs-lookup"><span data-stu-id="71c15-113">_fnevCriticalError_</span></span>
  
> <span data-ttu-id="71c15-114">セッションの実行中のシャット ダウンなど、グローバル エラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="71c15-114">A global error has occurred, such as a session shut down in progress.</span></span> <span data-ttu-id="71c15-115">**情報**のメンバーには、 [ERROR_NOTIFICATION](error_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-115">The **info** member contains an [ERROR_NOTIFICATION](error_notification.md) structure.</span></span> 
    
 <span data-ttu-id="71c15-116">_fnevExtended_</span><span class="sxs-lookup"><span data-stu-id="71c15-116">_fnevExtended_</span></span>
  
> <span data-ttu-id="71c15-117">特定のサービス プロバイダーによって定義されている内部のイベントが発生しました。</span><span class="sxs-lookup"><span data-stu-id="71c15-117">An internal event defined by a particular service provider has occurred.</span></span> <span data-ttu-id="71c15-118">**情報**のメンバーには、 [EXTENDED_NOTIFICATION](extended_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-118">The **info** member contains an [EXTENDED_NOTIFICATION](extended_notification.md) structure.</span></span> 
    
 <span data-ttu-id="71c15-119">_fnevNewMail_</span><span class="sxs-lookup"><span data-stu-id="71c15-119">_fnevNewMail_</span></span>
  
> <span data-ttu-id="71c15-120">メッセージが配信されましたが、該当するメッセージ クラスのフォルダーが表示され、処理されるを待っています。</span><span class="sxs-lookup"><span data-stu-id="71c15-120">A message has been delivered to the appropriate receive folder for the message class and is waiting to be processed.</span></span> <span data-ttu-id="71c15-121">**情報**のメンバーには、 [NEWMAIL_NOTIFICATION](newmail_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-121">The **info** member contains an [NEWMAIL_NOTIFICATION](newmail_notification.md) structure.</span></span> 
    
 <span data-ttu-id="71c15-122">_fnevObjectCopied_</span><span class="sxs-lookup"><span data-stu-id="71c15-122">_fnevObjectCopied_</span></span>
  
> <span data-ttu-id="71c15-123">MAPI オブジェクトがコピーされました。</span><span class="sxs-lookup"><span data-stu-id="71c15-123">A MAPI object has been copied.</span></span> <span data-ttu-id="71c15-124">**情報**のメンバーには、 [OBJECT_NOTIFICATION](object_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-124">The **info** member contains an [OBJECT_NOTIFICATION](object_notification.md) structure.</span></span> 
    
 <span data-ttu-id="71c15-125">_fnevObjectCreated_</span><span class="sxs-lookup"><span data-stu-id="71c15-125">_fnevObjectCreated_</span></span>
  
> <span data-ttu-id="71c15-126">MAPI オブジェクトが用意されています。</span><span class="sxs-lookup"><span data-stu-id="71c15-126">A MAPI object has been created.</span></span> <span data-ttu-id="71c15-127">**情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-127">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="71c15-128">_fnevObjectDeleted_</span><span class="sxs-lookup"><span data-stu-id="71c15-128">_fnevObjectDeleted_</span></span>
  
> <span data-ttu-id="71c15-129">MAPI オブジェクトが削除されました。</span><span class="sxs-lookup"><span data-stu-id="71c15-129">A MAPI object has been deleted.</span></span> <span data-ttu-id="71c15-130">**情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-130">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="71c15-131">_fnevObjectModified_</span><span class="sxs-lookup"><span data-stu-id="71c15-131">_fnevObjectModified_</span></span>
  
> <span data-ttu-id="71c15-132">MAPI オブジェクトが変更されました。</span><span class="sxs-lookup"><span data-stu-id="71c15-132">A MAPI object has changed.</span></span> <span data-ttu-id="71c15-133">**情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-133">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="71c15-134">_fnevObjectMoved_</span><span class="sxs-lookup"><span data-stu-id="71c15-134">_fnevObjectMoved_</span></span>
  
> <span data-ttu-id="71c15-135">メッセージ ストアやアドレス帳オブジェクトが移動されました。</span><span class="sxs-lookup"><span data-stu-id="71c15-135">A message store or address book object has been moved.</span></span> <span data-ttu-id="71c15-136">**情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-136">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="71c15-137">_fnevSearchComplete_</span><span class="sxs-lookup"><span data-stu-id="71c15-137">_fnevSearchComplete_</span></span>
  
> <span data-ttu-id="71c15-138">検索操作が完了し、結果が保存されます。</span><span class="sxs-lookup"><span data-stu-id="71c15-138">A search operation has finished and the results are available.</span></span> <span data-ttu-id="71c15-139">**情報**のメンバーには、 **OBJECT_NOTIFICATION**構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-139">The **info** member contains an **OBJECT_NOTIFICATION** structure.</span></span> 
    
 <span data-ttu-id="71c15-140">_fnevTableModified_</span><span class="sxs-lookup"><span data-stu-id="71c15-140">_fnevTableModified_</span></span>
  
> <span data-ttu-id="71c15-141">テーブル内の情報が変更されました。</span><span class="sxs-lookup"><span data-stu-id="71c15-141">Information in a table has changed.</span></span> <span data-ttu-id="71c15-142">**情報**のメンバーには、 [TABLE_NOTIFICATION](table_notification.md)構造体が含まれています。</span><span class="sxs-lookup"><span data-stu-id="71c15-142">The **info** member contains an [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    
<span data-ttu-id="71c15-143">**情報**</span><span class="sxs-lookup"><span data-stu-id="71c15-143">**info**</span></span>
  
> <span data-ttu-id="71c15-144">イベントの特定の種類の影響を受けるデータを記述する通知の構造体の共用体です。</span><span class="sxs-lookup"><span data-stu-id="71c15-144">Union of notification structures describing the affected data for a particular type of event.</span></span> <span data-ttu-id="71c15-145">**情報**のメンバーに含まれている構造体は、 **ulEventType**メンバーの値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="71c15-145">The structure included in the **info** member depends on the value of the **ulEventType** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="71c15-146">備考</span><span class="sxs-lookup"><span data-stu-id="71c15-146">Remarks</span></span>

<span data-ttu-id="71c15-147">1 つまたは複数の**通知**の構造体は、登録されているアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すたびに、入力パラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="71c15-147">One or more **NOTIFICATION** structures are passed as input parameters with every call to a registered advise sink's [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="71c15-148">**通知**の構造体は、発生し、影響を受けるオブジェクトについて説明する特定のイベントに関する情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="71c15-148">The **NOTIFICATION** structures contain information about the particular events that have occurred and describe the affected objects.</span></span> 
  
<span data-ttu-id="71c15-149">クライアントまたはサービス プロバイダーが通知の受信の場合は、イベントを処理する構造を使用できます、前に、イベントの種類を確認して、 **ulEventType**メンバーに示されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="71c15-149">Before clients or service providers receiving a notification can use the structure to process the event, they must check the event type as indicated in the **ulEventType** member.</span></span> <span data-ttu-id="71c15-150">たとえば、ここでの新しいメッセージと、この種類のイベントを検出すると、到着の確認が表示されているコード サンプルは、メッセージのメッセージ クラスを出力します。</span><span class="sxs-lookup"><span data-stu-id="71c15-150">For example, the code sample that is shown here checks for the arrival of a new message and upon detecting an event of this kind, prints out the message class of the message.</span></span> 
  
```cpp
if (pNotif -> ulEventType == fnevNewMail)
{
printf("%s\n", pNotif -> newmail.lpszMessageClass)
}

```

<span data-ttu-id="71c15-151">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="71c15-151">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="71c15-152">**トピック**</span><span class="sxs-lookup"><span data-stu-id="71c15-152">**Topic**</span></span>|<span data-ttu-id="71c15-153">**説明**</span><span class="sxs-lookup"><span data-stu-id="71c15-153">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="71c15-154">MAPI でのイベントの通知</span><span class="sxs-lookup"><span data-stu-id="71c15-154">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="71c15-155">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="71c15-155">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="71c15-156">通知の処理</span><span class="sxs-lookup"><span data-stu-id="71c15-156">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="71c15-157">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="71c15-157">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="71c15-158">イベント通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="71c15-158">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="71c15-159">サービス プロバイダーが、 [IMAPISupport](imapisupportiunknown.md)メソッドを使用して、通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="71c15-159">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) method to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71c15-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="71c15-160">See also</span></span>


- [<span data-ttu-id="71c15-161">ERROR_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="71c15-161">ERROR_NOTIFICATION</span></span>](error_notification.md)  
- [<span data-ttu-id="71c15-162">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="71c15-162">EXTENDED_NOTIFICATION</span></span>](extended_notification.md)  
- [<span data-ttu-id="71c15-163">NEWMAIL_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="71c15-163">NEWMAIL_NOTIFICATION</span></span>](newmail_notification.md)  
- [<span data-ttu-id="71c15-164">OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="71c15-164">OBJECT_NOTIFICATION</span></span>](object_notification.md)  
- [<span data-ttu-id="71c15-165">STATUS_OBJECT_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="71c15-165">STATUS_OBJECT_NOTIFICATION</span></span>](status_object_notification.md)  
- [<span data-ttu-id="71c15-166">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="71c15-166">TABLE_NOTIFICATION</span></span>](table_notification.md)
- [<span data-ttu-id="71c15-167">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="71c15-167">MAPI Structures</span></span>](mapi-structures.md)

