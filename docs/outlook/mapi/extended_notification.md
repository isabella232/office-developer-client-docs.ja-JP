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
ms.openlocfilehash: de9b5e377840b1fbfa3b6dd73fd952c0c72efeb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580643"
---
# <a name="extendednotification"></a><span data-ttu-id="64a3c-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="64a3c-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="64a3c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64a3c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64a3c-105">サービス プロバイダーに固有ではイベントに関連する情報をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="64a3c-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64a3c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="64a3c-106">Header file:</span></span>  <br/> |<span data-ttu-id="64a3c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="64a3c-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="64a3c-108">Members</span><span class="sxs-lookup"><span data-stu-id="64a3c-108">Members</span></span>

 <span data-ttu-id="64a3c-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="64a3c-109">**ulEvent**</span></span>
  
> <span data-ttu-id="64a3c-110">プロバイダーによって定義されている拡張イベント コードです。</span><span class="sxs-lookup"><span data-stu-id="64a3c-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="64a3c-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="64a3c-111">**cb**</span></span>
  
> <span data-ttu-id="64a3c-112">**PbEventParameters**が指すイベントに固有のパラメーターのバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="64a3c-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="64a3c-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="64a3c-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="64a3c-114">イベント固有のパラメーターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="64a3c-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="64a3c-115">使用されるパラメーターの型は、 **ulEvent**メンバーの値によって異なります。イベントを発行したプロバイダーによっては、これらのパラメーターが記載されています。</span><span class="sxs-lookup"><span data-stu-id="64a3c-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="64a3c-116">注釈</span><span class="sxs-lookup"><span data-stu-id="64a3c-116">Remarks</span></span>

<span data-ttu-id="64a3c-117">**EXTENDED_NOTIFICATION**構造では、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="64a3c-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="64a3c-118">**通知**の構造体のメンバー**情報**には、 **EXTENDED_NOTIFICATION**構造体が含まれている、**通知**の構造体の**ulEventType**メンバーは、 _fnevExtended_に設定されています。</span><span class="sxs-lookup"><span data-stu-id="64a3c-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="64a3c-119">拡張イベントは、他の定義済みのイベントのいずれかで対応できない変更のタイプを表すためのサービス プロバイダーによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="64a3c-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="64a3c-120">拡張イベントをサポートしているサービス プロバイダーを登録する前に知っているクライアントのみがそのイベントに対して登録できます。</span><span class="sxs-lookup"><span data-stu-id="64a3c-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="64a3c-121">クライアント サービス プロバイダーは、拡張イベントをサポートしている高度な知識がないかを確認することはできません。</span><span class="sxs-lookup"><span data-stu-id="64a3c-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="64a3c-122">サービス プロバイダーは、拡張イベントをサポートする場合は、受信したときにこのようなイベントを処理する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="64a3c-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="64a3c-123">クライアントがログオフしたときのセッションでは、拡張の通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="64a3c-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="64a3c-124">_LpEntryID_パラメーターを NULL に設定され、 _cbEntryID_パラメーターを 0 に設定で[IMAPISession::Advise](imapisession-advise.md)を呼び出すことによって、この通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="64a3c-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="64a3c-125">通知の詳細については、次の表に記載されているトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="64a3c-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="64a3c-126">**トピック**</span><span class="sxs-lookup"><span data-stu-id="64a3c-126">**Topic**</span></span>|<span data-ttu-id="64a3c-127">**説明**</span><span class="sxs-lookup"><span data-stu-id="64a3c-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64a3c-128">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="64a3c-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="64a3c-129">通知と通知のイベントの概要です。</span><span class="sxs-lookup"><span data-stu-id="64a3c-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="64a3c-130">通知の処理</span><span class="sxs-lookup"><span data-stu-id="64a3c-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="64a3c-131">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64a3c-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="64a3c-132">イベント通知のサポート</span><span class="sxs-lookup"><span data-stu-id="64a3c-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="64a3c-133">サービス ・ プロバイダーが通知を生成する[IMAPISupport](imapisupportiunknown.md)メソッドを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64a3c-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64a3c-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="64a3c-134">See also</span></span>



[<span data-ttu-id="64a3c-135">�ʒm</span><span class="sxs-lookup"><span data-stu-id="64a3c-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="64a3c-136">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="64a3c-136">MAPI Structures</span></span>](mapi-structures.md)

