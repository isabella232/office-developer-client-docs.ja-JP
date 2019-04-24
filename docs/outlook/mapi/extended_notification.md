---
title: EXTENDED_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.EXTENDED_NOTIFICATION
api_type:
- COM
ms.assetid: f01fce7b-a038-4002-8bad-0e6a51ae9d05
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341119"
---
# <a name="extendednotification"></a><span data-ttu-id="9ff28-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="9ff28-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="9ff28-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9ff28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9ff28-105">サービスプロバイダー固有のイベントに関連する情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ff28-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ff28-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9ff28-106">Header file:</span></span>  <br/> |<span data-ttu-id="9ff28-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9ff28-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="9ff28-108">Members</span><span class="sxs-lookup"><span data-stu-id="9ff28-108">Members</span></span>

 <span data-ttu-id="9ff28-109">**ulevent**</span><span class="sxs-lookup"><span data-stu-id="9ff28-109">**ulEvent**</span></span>
  
> <span data-ttu-id="9ff28-110">プロバイダーによって定義された拡張イベントコード。</span><span class="sxs-lookup"><span data-stu-id="9ff28-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="9ff28-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="9ff28-111">**cb**</span></span>
  
> <span data-ttu-id="9ff28-112">**p傾斜 entparameters**で示されるイベント固有のパラメーターのバイト数。</span><span class="sxs-lookup"><span data-stu-id="9ff28-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="9ff28-113">**p斜め entparameters**</span><span class="sxs-lookup"><span data-stu-id="9ff28-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="9ff28-114">イベント固有のパラメーターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="9ff28-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="9ff28-115">使用されるパラメーターの型は**ulevent**メンバーの値に依存します。これらのパラメーターは、イベントを発行したプロバイダーによってドキュメント化されます。</span><span class="sxs-lookup"><span data-stu-id="9ff28-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9ff28-116">解説</span><span class="sxs-lookup"><span data-stu-id="9ff28-116">Remarks</span></span>

<span data-ttu-id="9ff28-117">**EXTENDED_NOTIFICATION**構造体は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="9ff28-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="9ff28-118">**通知**構造の**info**メンバーに**EXTENDED_NOTIFICATION**構造体が含まれている場合、**通知**構造の**uleventtype**メンバーは_fnevExtended_に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9ff28-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="9ff28-119">拡張イベントは、サービスプロバイダーによって定義され、他のどの定義済みイベントによってもカバーできない変更の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="9ff28-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="9ff28-120">サービスプロバイダーが拡張イベントをサポートすることを登録する前に知っているクライアントのみが、そのイベントの登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="9ff28-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="9ff28-121">サービスプロバイダーが拡張イベントをサポートしている場合、クライアントは高度な知識がなくても判断できません。</span><span class="sxs-lookup"><span data-stu-id="9ff28-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="9ff28-122">サービスプロバイダーが拡張イベントをサポートしている場合は、受信時にこのようなイベントを処理する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9ff28-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="9ff28-123">クライアントがログオフすると、セッションによって拡張通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="9ff28-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="9ff28-124">この通知を登録するには、 _lpentryid_パラメーターを NULL に設定し、 _cbEntryID_パラメーターを0に設定して、 [imapitryid](imapisession-advise.md)パラメーターを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9ff28-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="9ff28-125">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ff28-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="9ff28-126">**トピック**</span><span class="sxs-lookup"><span data-stu-id="9ff28-126">**Topic**</span></span>|<span data-ttu-id="9ff28-127">**説明**</span><span class="sxs-lookup"><span data-stu-id="9ff28-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9ff28-128">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="9ff28-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="9ff28-129">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="9ff28-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="9ff28-130">通知の処理</span><span class="sxs-lookup"><span data-stu-id="9ff28-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="9ff28-131">クライアントが通知を処理する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="9ff28-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="9ff28-132">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="9ff28-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="9ff28-133">サービスプロバイダーが[imapisupport](imapisupportiunknown.md)方法を使用して通知を生成する方法についての説明。</span><span class="sxs-lookup"><span data-stu-id="9ff28-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9ff28-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ff28-134">See also</span></span>



[<span data-ttu-id="9ff28-135">�ʒm</span><span class="sxs-lookup"><span data-stu-id="9ff28-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="9ff28-136">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9ff28-136">MAPI Structures</span></span>](mapi-structures.md)

