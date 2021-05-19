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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a8b49d0b80102f6295f3f717fb123a6581854d5a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415720"
---
# <a name="extended_notification"></a><span data-ttu-id="df106-103">EXTENDED_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="df106-103">EXTENDED_NOTIFICATION</span></span>

  
  
<span data-ttu-id="df106-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df106-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df106-105">サービス プロバイダー固有のイベントに関連する情報を説明します。</span><span class="sxs-lookup"><span data-stu-id="df106-105">Describes information that relates to an event that is service provider-specific.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="df106-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="df106-106">Header file:</span></span>  <br/> |<span data-ttu-id="df106-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df106-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _EXTENDED_NOTIFICATION
{
  ULONG ulEvent;
  ULONG cb;
  LPBYTE pbEventParameters;
} EXTENDED_NOTIFICATION;

```

## <a name="members"></a><span data-ttu-id="df106-108">Members</span><span class="sxs-lookup"><span data-stu-id="df106-108">Members</span></span>

 <span data-ttu-id="df106-109">**ulEvent**</span><span class="sxs-lookup"><span data-stu-id="df106-109">**ulEvent**</span></span>
  
> <span data-ttu-id="df106-110">プロバイダーによって定義される拡張イベント コード。</span><span class="sxs-lookup"><span data-stu-id="df106-110">Extended event code that is defined by the provider.</span></span>
    
 <span data-ttu-id="df106-111">**cb**</span><span class="sxs-lookup"><span data-stu-id="df106-111">**cb**</span></span>
  
> <span data-ttu-id="df106-112">**pbEventParameters** が指すイベント固有のパラメーターのバイト数です。</span><span class="sxs-lookup"><span data-stu-id="df106-112">Count of bytes in the event-specific parameters pointed to by **pbEventParameters**.</span></span> 
    
 <span data-ttu-id="df106-113">**pbEventParameters**</span><span class="sxs-lookup"><span data-stu-id="df106-113">**pbEventParameters**</span></span>
  
> <span data-ttu-id="df106-114">イベント固有のパラメーターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="df106-114">Pointer to event-specific parameters.</span></span> <span data-ttu-id="df106-115">使用されるパラメーターの種類は **、ulEvent メンバーの値によって異** なります。これらのパラメーターは、イベントを発行したプロバイダーによって文書化されます。</span><span class="sxs-lookup"><span data-stu-id="df106-115">The type of parameters that are used depends on the value of the **ulEvent** member; these parameters are documented by the provider that issued the event.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="df106-116">注釈</span><span class="sxs-lookup"><span data-stu-id="df106-116">Remarks</span></span>

<span data-ttu-id="df106-117">この **EXTENDED_NOTIFICATION** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体 **のメンバー** の [1](notification.md) つです。</span><span class="sxs-lookup"><span data-stu-id="df106-117">The **EXTENDED_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="df106-118">**NOTIFICATION** 構造体 **の info** メンバーに EXTENDED_NOTIFICATION構造が含まれている場合 **、NOTIFICATION** 構造体の **ulEventType** メンバーは _fnevExtended に設定されます_。</span><span class="sxs-lookup"><span data-stu-id="df106-118">When the **info** member of a **NOTIFICATION** structure contains an **EXTENDED_NOTIFICATION** structure, the **ulEventType** member of the **NOTIFICATION** structure is set to  _fnevExtended_.</span></span>
  
<span data-ttu-id="df106-119">拡張イベントは、他の定義済みイベントではカバーできない変更の種類を表すサービス プロバイダーによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="df106-119">The extended event is defined by a service provider to represent a type of change that cannot be covered by any of the other predefined events.</span></span> <span data-ttu-id="df106-120">サービス プロバイダーが拡張イベントをサポートすると登録する前に知っているクライアントだけが、そのイベントに登録できます。</span><span class="sxs-lookup"><span data-stu-id="df106-120">Only clients that know before they register that a service provider supports an extended event can register for that event.</span></span> <span data-ttu-id="df106-121">サービス プロバイダーが拡張イベントをサポートしている場合、クライアントは高度な知識なしに判断できない。</span><span class="sxs-lookup"><span data-stu-id="df106-121">It is not possible for clients to determine without advanced knowledge if a service provider supports an extended event.</span></span> <span data-ttu-id="df106-122">サービス プロバイダーが拡張イベントをサポートしている場合は、受信時にそのようなイベントを処理する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="df106-122">If a service provider supports an extended event, it shows how to handle such an event when it is received.</span></span>
  
<span data-ttu-id="df106-123">クライアントがログオフすると、セッションによって拡張通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="df106-123">An extended notification is sent by the session when a client logs off.</span></span> <span data-ttu-id="df106-124">[IMAPISession::Advise](imapisession-advise.md)を呼び出して、この通知に登録し _、lpEntryID_ パラメーターを NULL に設定し _、cbEntryID_ パラメーターを 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="df106-124">Register for this notification by calling [IMAPISession::Advise](imapisession-advise.md) with the  _lpEntryID_ parameter set to NULL and the  _cbEntryID_ parameter set to zero.</span></span> 
  
<span data-ttu-id="df106-125">通知の詳細については、次の表で説明するトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="df106-125">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="df106-126">**トピック**</span><span class="sxs-lookup"><span data-stu-id="df106-126">**Topic**</span></span>|<span data-ttu-id="df106-127">**説明**</span><span class="sxs-lookup"><span data-stu-id="df106-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df106-128">MAPI のイベント通知</span><span class="sxs-lookup"><span data-stu-id="df106-128">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="df106-129">通知イベントと通知イベントの一般的な概要。</span><span class="sxs-lookup"><span data-stu-id="df106-129">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="df106-130">通知の処理</span><span class="sxs-lookup"><span data-stu-id="df106-130">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="df106-131">クライアントが通知を処理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="df106-131">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="df106-132">サポート イベント通知</span><span class="sxs-lookup"><span data-stu-id="df106-132">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="df106-133">サービス プロバイダーが [IMAPISupport](imapisupportiunknown.md) メソッドを使用して通知を生成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="df106-133">Discussion of how service providers can use the [IMAPISupport](imapisupportiunknown.md) methods to generate notifications.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df106-134">関連項目</span><span class="sxs-lookup"><span data-stu-id="df106-134">See also</span></span>



[<span data-ttu-id="df106-135">�ʒm</span><span class="sxs-lookup"><span data-stu-id="df106-135">NOTIFICATION</span></span>](notification.md)


[<span data-ttu-id="df106-136">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="df106-136">MAPI Structures</span></span>](mapi-structures.md)

